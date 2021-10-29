<template>
  <footer class="footer -mx-4 md:mx-0">
    <div class="container mx-auto pb-6 flex justify-center flex-col">
      <div class="w-full"><img src="/images/uploads/footer.png" alt="" /></div>
      <div class="flex flex-row justify-center">
        <a href="" class="px-5">World</a>
        <span>|</span>
        <a href="" class="px-5">Site</a>
      </div>
      <div class="text-center mx-20 px-20 py-10">
        <p>
          A limited collection where the NFT is a membership and governance token to the Gods of
          Block Artverse, a play-to-earn project that gamifies the building of communities to
          support artists and collectors
        </p>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component
export default class Footer extends Vue {}
</script>

<style lang="scss">
.footer {
  // background-color: $bluise;
}
</style>
