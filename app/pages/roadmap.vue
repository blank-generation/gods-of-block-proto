<template>
  <div>
    <h2 class="text-center title">Road Map</h2>
    <div class="flex roadmapCont">
      <div class="flex flex-col justify-items-center">
        <!-- Section 1 -->
        <div class="flex flex-col md:flex-row justify-center justify-items-center gap-x-20">
          <div class="justify-items-center flex justify-center md:w-1/2">
            <img
              src="/images/uploads/roadmap_bllock-01.svg"
              alt=""
              class="hidden md:block timeBullet"
            />
            <img src="/images/uploads/25p-01.svg" alt="" class="svg-img" />
          </div>
          <div class="md:p-24 p-10">
            <h2>25% GENESIS COLLECTION</h2>
            <p class="">
              The Block God Generator is released and will enable the community to create their own
              Gods. The Gods created will be voted on by the community and minted. The creator gets
              50% of the proceeds when their God is minted and sold.
            </p>
          </div>
        </div>
        <!-- Section 2 -->
        <div class="flex flex-col md:flex-row justify-center justify-items-center gap-x-20">
          <div class="justify-items-center flex justify-center">
            <img
              src="/images/uploads/roadmap_bllock-01.svg"
              alt=""
              class="hidden md:block timeBullet"
            />
            <img src="/images/uploads/50p-01.svg" alt="" class="svg-img" />
          </div>
          <div class="my-auto p-10 md:px-24">
            <h2>50% GENESIS COLLECTION</h2>
            <p>
              Voting on artists for the community who will design specific features of the Artverse
              will begin 100% Genesis Collection Sale - The building of the Artverse will begin. We
              will start with intimate conversations between designers/artists and the community.
              The community will play a continuous guiding role in the building of the Artverse.
            </p>
          </div>
        </div>
        <!-- Section 3 -->
        <div class="flex flex-col md:flex-row justify-center justify-items-center gap-x-20">
          <div class="justify-items-center flex justify-center">
            <img
              src="/images/uploads/roadmap_bllock-01.svg"
              alt=""
              class="hidden md:block timeBullet"
            />
            <img src="/images/uploads/100p-01.svg" alt="" class="svg-img" />
          </div>
          <div class="textCont my-auto p-10 md:p-24">
            <h2>100% GENESIS COLLECTION</h2>
            <p>
              The building of the Artverse will begin. We will start with intimate conversations
              between designers/artists and the community. The community will play a continuous
              guiding role in the building of the Artverse.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {};
</script>

<style lang="scss">
@media (max-width: 800px) {
  .fancyDiv {
    display: none;
  }
  .svg-img {
    /* max-width: 100%;
    max-height: 100%; */
    /* padding: 20px; */
    // width: 300px;
  }
}

.svg-img {
  /* max-width: 35vw;
  padding: 20px; */
  width: 600px;
  // margin: 20px;
}
.roadmapCont {
  border-left: 1px solid white;
  /* z-index: 1; */
}

.timeBullet {
  width: 60px;
  z-index: 1000;
}
h2.title {
  font-size: 36px;
}

.roadmapCont h2 {
  color: #fab317;
}
</style>
