<template>
  <!-- <div class="container my-10 pb-6 mx-0 flex justify-center flex-col">
    <Landing />
  </div> -->
  <div class="flex h-screen teamCont">
    <div class="m-auto">
      <img src="/images/uploads/Gods_of_Block_only_text.svg" alt="" />
      <h2 class="text-center">COMING SOON</h2>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
// import Landing from '@/components/landing.vue';
// import settings from '@/content/settings/general.json';

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

<style></style>
