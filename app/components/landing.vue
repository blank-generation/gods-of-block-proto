<template>
  <canvas id="worldCanvas"></canvas>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import * as THREE from 'three';
import { Scene, Camera, WebGLRenderer } from 'three';
// eslint-disable-next-line import/extensions
// import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js';
// import { SVGLoader } from 'three/examples/jsm/loaders/SVGLoader';
import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls';

@Component
export default class Landing extends Vue {
  name = 'Landing';

  scene: Scene;

  bgscene: Scene;

  camera: Camera;

  bgcam: Camera;

  renderer: WebGLRenderer;

  shmat;

  skymesh;

  sky;

  sceneLoaded = false;

  pl1;

  pl2;

  pl3;

  pl4;

  directionalLight;

  controls;

  public init(): void {
    this.scene = new THREE.Scene();
    this.bgscene = new THREE.Scene();
    this.camera = new THREE.PerspectiveCamera(75, 2, 0.1, 1000);
    this.bgcam = new THREE.PerspectiveCamera(75, 2, 0.1, 1000);
    const canvas = document.querySelector('#worldCanvas');
    this.renderer = new THREE.WebGLRenderer({ canvas });
    // this.renderer.setSize(window.innerWidth * 0.9, window.innerHeight * 0.9);
    this.renderer.antialias = true;
    // const cont = document.getElementById('3dSec');
    // const loader = new GLTFLoader();
    // loader.load(
    //   '/models/blockGodSet1.glb',
    //   (gltf): void => {
    //     gltf.scene.position.set(-1.4, -1, 0);
    //     this.scene.add(gltf.scene);
    //   },
    //   undefined,
    //   (error): void => {
    //     console.error(error);
    //   }
    // );
    // if (cont != null) {
    //   cont.append(this.renderer.domElement);
    // }
    const vsh = `precision highp float;
              varying vec2 vUv;
              varying vec3 vNormal;

              /*------------------------------
              Main
              ------------------------------*/
              void main() {
                vUv = uv;
                vNormal = normal;
                vec4 mvPosition = modelViewMatrix * vec4(position, 1.);
                gl_Position = projectionMatrix * mvPosition;
              }               
    `;
    const fsh = `
        #define iterations 10
        #define formuparam 0.53

        #define volsteps 20
        #define stepsize 0.2

        #define zoom   0.800
        #define tile   0.900
        #define speed  0.001 

        #define brightness 0.0015
        #define darkmatter 0.300
        #define distfading 0.730
        #define saturation 0.850

        
        precision highp float;
          varying vec2 vUv;
          uniform vec3 uColor;
          uniform float u_time;
          varying vec3 vNormal;

 

          void main() {
            vec2 uv = vUv;
            float iTime = u_time;
            vec3 dir=vec3(uv*zoom,1.);
          	float time=iTime*speed+.25;
            float s=0.1,fade=1.;
            vec3 v=vec3(0.);
            vec3 from=vec3(1.,.5,0.5);
            from+=vec3(time*2.,time,-2.);
            for (int r=0; r<volsteps; r++) {
              vec3 p=from+s*dir*.5;
              p = abs(vec3(tile)-mod(p,vec3(tile*2.))); // tiling fold
              float pa,a=pa=0.;
              for (int i=0; i<iterations; i++) { 
                p=abs(p)/dot(p,p)-formuparam; // the magic formula
                a+=abs(length(p)-pa); // absolute sum of average change
                pa=length(p);
              }
              float dm=max(0.,darkmatter-a*a*.001); //dark matter
              a*=a*a; // add contrast
              if (r>6) fade*=1.-dm; // dark matter, don't render near
              //v+=vec3(dm,dm*.5,0.);
              v+=fade;
              v+=vec3(s,s*s,s*s*s*s)*a*brightness*fade; // coloring based on distance
              fade*=distfading; // distance fading
              s+=stepsize;
            }
            v=mix(vec3(length(v)),v,saturation); //color adjust
            gl_FragColor = vec4(v*.01, 1.);
          }`;
    this.directionalLight = new THREE.DirectionalLight(0xffffff, 1.5);
    this.directionalLight.rotation.x = 60;
    this.scene.add(this.directionalLight);
    this.pl1 = new THREE.PointLight(0xffffff, 1);
    this.pl1.position.set(0, 0, -3);
    this.pl2 = new THREE.PointLight(0xffffff, 1);
    this.pl2.position.set(0, 0, 6);
    this.pl3 = new THREE.PointLight(0xffffff, 1);
    this.pl3.position.set(-3, 0, 0);
    this.pl4 = new THREE.PointLight(0xffffff, 1);
    this.pl4.position.set(3, 0, 0);
    this.scene.add(this.pl1, this.pl2, this.pl3, this.pl4);
    this.controls = new OrbitControls(this.camera, this.renderer.domElement);

    this.shmat = new THREE.ShaderMaterial({
      uniforms: {
        u_time: { value: 1.0 },
        resolution: { value: new THREE.Vector2() },
      },

      vertexShader: vsh,

      fragmentShader: fsh,
    });
    // const svgloader = new SVGLoader();

    // load a SVG resource
    // svgloader.load(
    //   // resource URL
    //   'images/uploads/coming_soon_bg-01.svg',
    //   // called when the resource is loaded
    //   (data) => {
    //     const { paths } = data;
    //     const group = new THREE.Group();

    //     for (let i = 0; i < paths.length; i += 1) {
    //       const path = paths[i];

    //       const material = new THREE.MeshBasicMaterial({
    //         color: path.color,
    //         side: THREE.DoubleSide,
    //         depthWrite: false,
    //       });

    //       const shapes = SVGLoader.createShapes(path);

    //       for (let j = 0; j < shapes.length; j += 1) {
    //         const shape = shapes[j];
    //         const geometry = new THREE.ShapeGeometry(shape);
    //         const mesh = new THREE.Mesh(geometry, material);
    //         group.add(mesh);
    //       }
    //       this.bgscene.add(group);
    //     }
    //   }
    // );
    this.sky = new THREE.PlaneGeometry(30, 30);
    this.skymesh = new THREE.Mesh(this.sky, this.shmat);
    this.sky.dispose();
    this.shmat.dispose();
    this.skymesh.position.z = -5;
    this.bgscene.add(this.skymesh);
    this.camera.position.z = 5;
    this.bgcam.position.z = 5;
    this.controls.update();
  }

  animate(): void {
    requestAnimationFrame(this.animate);
    if (this.resizeRendererToDisplaySize()) {
      const canvas = this.renderer.domElement;
      this.camera.aspect = canvas.clientWidth / canvas.clientHeight;
      this.bgcam.aspect = canvas.clientWidth / canvas.clientHeight;
      this.bgcam.updateProjectionMatrix();
      this.camera.updateProjectionMatrix();
    }
    this.shmat.uniforms.u_time.value += 0.1;
    this.renderer.autoClear = false;
    this.renderer.clear();
    this.renderer.render(this.bgscene, this.bgcam);
    this.renderer.render(this.scene, this.camera);
    this.sceneLoaded = true;
  }

  resizeRendererToDisplaySize(): boolean {
    const canvas = this.renderer.domElement;
    const width = canvas.clientWidth;
    const height = canvas.clientHeight;
    const needResize = canvas.width !== width || canvas.height !== height;
    if (needResize) {
      this.renderer.setSize(width, height, false);
    }
    return needResize;
  }

  clearScene(): void {
    this.shmat.dispose();
    this.sky.dispose();
    this.skymesh.material.dispose();
    this.skymesh.geometry.dispose();
    this.shmat.dispose();
    this.pl1.dispose();
    this.pl2.dispose();
    this.pl3.dispose();
    this.pl4.dispose();
    this.directionalLight.dispose();
    // this.scene.dispose();
    // this.bgscene.dispose();
    this.renderer.dispose();
    this.controls.dispose();
  }

  mounted(): void {
    this.init();
    this.animate();
    // console.log('SceneLoaded');
  }

  beforeDestroy(): void {
    this.clearScene();
  }
}
</script>

<style lang="scss">
#worldCanvas {
  width: 100%;
  height: 70vh;
}
</style>
