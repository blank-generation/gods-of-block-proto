<template>
  <section class="home">
    <!-- <Landing></Landing> -->
    <div
      class="
        py-10
        md:py-0
        mx-auto
        flex flex-wrap flex-col
        md:flex-row
        items-center
        align-middle
        sec1
      "
    >
      <div
        class="
          flex
          lg:flex-row
          flex-col
          w-full
          justify-center
          lg:items-center
          overflow-y-hidden
          align-middle
        "
      >
        <div class="lg:w-full"><img :src="welcomeImg" alt="" /></div>
        <div v-html="$md.render(welcomeText)" class="home__welcome markdown lg:w-1/2 lg:pl-20" />
      </div>
    </div>
    <!-- Section 2 -->
    <div
      class="
        py-10
        md:py-0
        mx-auto
        flex flex-wrap flex-col
        md:flex-row
        items-center
        align-middle
        sec2
        sec
      "
    >
      <div
        class="
          flex
          lg:flex-row
          flex-col
          w-full
          justify-center
          lg:items-center
          overflow-y-hidden
          align-middle
        "
      >
        <div class="lg:w-full"><img :src="img2" alt="" /></div>
        <div v-html="$md.render(para2)" class="home__welcome markdown lg:w-1/2 lg:pl-20" />
      </div>
    </div>
    <!-- Section 3 -->
    <div
      class="
        py-10
        md:py-0
        mx-auto
        flex flex-wrap flex-col
        md:flex-row
        items-center
        align-middle
        sec3
        sec
      "
    >
      <div
        class="
          flex
          lg:flex-row
          flex-col
          w-full
          justify-center
          lg:items-center
          overflow-y-hidden
          align-middle
        "
      >
        <div class="lg:w-full"><img :src="img3" alt="" /></div>
        <div v-html="$md.render(para3)" class="home__welcome markdown lg:w-1/2 lg:pl-20" />
      </div>
    </div>
    <!-- Section 4 -->
    <div
      class="
        py-10
        md:py-0
        mx-auto
        flex flex-wrap flex-col
        md:flex-row
        items-center
        align-middle
        sec4
        sec
      "
    >
      <div
        class="
          flex
          lg:flex-row
          flex-col
          w-full
          justify-center
          lg:items-center
          overflow-y-hidden
          align-middle
        "
      >
        <div class="lg:w-full"><img :src="img4" alt="" /></div>
        <div v-html="$md.render(para4)" class="home__welcome markdown lg:w-1/2 lg:pl-20" />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
  components: {
    // Landing,
  },
})
export default class Home extends Vue {
  welcomeText = settings.welcomeText;

  welcomeImg = settings.welcomeImage;

  para2 = settings.para2;

  para3 = settings.para3;

  para4 = settings.para4;

  img2 = settings.image2;

  img3 = settings.image3;

  img4 = settings.image4;

  $gsap;

  animateOnScroll(): void {
    this.$gsap.utils.toArray('.sec').forEach((element) => {
      this.$gsap.from(element.querySelectorAll('img'), {
        skewX: 1,
        skewY: 1,
        rotate: 4,
        // y: -50,
        y: -60,
        opacity: 0,
        scrollTrigger: {
          trigger: element.querySelectorAll('img'),
          pin: true,
          // markers: true,
          // pinSpacing: false,
          start: 'top top',
          end: 'bottom center',
          scrub: true,
        },
      });
      this.$gsap.fromTo(
        element.querySelectorAll('p'),
        {
          ease: 'elastic.out(1,0.3)',
          scale: 1,
          skewY: 1,
          autoAlpha: 0,
        },
        {
          scale: 1.05,
          skewY: -1,
          autoAlpha: 1,
          scrollTrigger: {
            trigger: element.querySelectorAll('p'),
            duration: 2,
            toggleActions: 'play play play play',
            // pin: true,
            start: 'top center',
            end: 'bottom',
            scrub: true,
          },
        }
      );
      this.$gsap.to(element.querySelectorAll('h2'), {
        scale: 1.2,
        skewY: -2,
        opacity: 1,
        x: -20,
        // y: -30,
        scrollTrigger: {
          trigger: element.querySelectorAll('h2'),
          // duration: 4,
          // pin: true,
          start: 'top center',
          // end: 'bottom',
          scrub: true,
        },
      });
    });
    this.$gsap.from('.sec1 img', {
      // ease: 'Power1.easeOut',
      // scale: 1.5,
      skewX: 4,
      skewY: 4,
      x: -50,
      rotation: -3,
      opacity: 0,
      scrollTrigger: {
        trigger: '.sec1',
        // pin: true,
        // markers: true,
        // start: 'top top',
        end: 'bottom',
        scrub: true,
      },
    });
    this.$gsap.fromTo(
      '.sec1 p',
      {
        ease: 'elastic.out(1,0.3)',
        scale: 1,
        skewY: 0,
        // autoAlpha: 0,
      },
      {
        scale: 1.05,
        skewY: -1,
        // autoAlpha: 1,
        scrollTrigger: {
          trigger: '.sec1',
          duration: 2,
          toggleActions: 'play none play none',
          // pin: true,
          start: 'top center',
          end: 'bottom',
          scrub: true,
        },
      }
    );
    this.$gsap.fromTo(
      '.sec1 h2',
      {
        ease: 'Power1.easeInOut',
        scale: 1,
        skewY: 0,
        x: 0,
        // opacity: 0,
      },
      {
        scale: 1.2,
        skewY: -1,
        x: -10,
        // opacity: 1,
        // y: -30,
        scrollTrigger: {
          trigger: '.sec1',
          // duration: 4,
          // pin: true,
          start: 'top center',
          // end: 'bottom',
          scrub: true,
        },
      }
    );
  }

  mounted(): void {
    this.animateOnScroll();
  }
}
</script>

<style>
.sec2 div,
.sec1 div,
.sec3 div,
.sec4 div {
  overflow: hidden;
}
</style>
