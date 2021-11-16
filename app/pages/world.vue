<template>
  <!-- <div class="container my-10 pb-6 mx-0 flex justify-center flex-col">
   
  </div> -->
  <div class="flex h-screen teamCont">
    <div class="w-full"><Landing class="m-auto landing" /></div>
    <div class="m-auto comingSoon absolute">
      <!-- <img src="/images/uploads/coming_soon_bg-01.svg" class="bgimg" alt="" /> -->
      <img src="/images/uploads/Gods_of_Block_only_text.svg" alt="" />
      <h2 class="text-center">COMING SOON</h2>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import Landing from '@/components/landing.vue';
// import settings from '@/content/settings/general.json';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
  components: {
    Landing,
  },
})
export default class Home extends Vue {
  $gsap;

  animateOnScroll(): void {
    // this.$gsap.to('rect', 3, { rotation: '360', ease: 'Power0.easeNone', repeat: -1 });
    // this.$gsap.to('circle', 3.2, { rotation: '360', ease: 'Power0.easeNone', repeat: -1 });
    // this.$gsap.to('polyline', 3.6, { rotation: '-360', ease: 'Power0.easeNone', repeat: -1 });
  }

  mounted(): void {
    this.animateOnScroll();
  }
}
</script>

<style>
.teamCont {
  /* background-image: linear-gradient(rgba(255, 255, 255, 0.5), rgba(255, 255, 255, 0.5)),
    url('/images/uploads/coming_soon_bg-01.svg'); */
  background-size: cover;
  background-position-x: center;
  /* height: 100vh; */
  font-size: 24px;
}

.landing {
  /* z-index: 0; */
}

.comingSoon {
  opacity: 0.9;
  top: 50%;
  left: 45%;
}
/* .bgimg {
  position: absolute;
  top: 100px;
  left: 100px;
} */
/* .comingSoon img {
  opacity: 0.2;
} */
</style>
