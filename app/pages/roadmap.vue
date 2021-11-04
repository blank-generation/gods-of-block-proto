<template>
  <div>
    <!-- <h2>Road Map</h2> -->
    <!-- Section 1 -->
    <div class="flex lg:flex-row flex-col space-x-10 py-10 px-10">
      <img src="/images/uploads/roadmap-01.svg" alt="" class="svg-img lg:w-1/3" />
      <img src="/images/uploads/roadmap-04.svg" class="fancyDiv lg:w-1/3" alt="" />
      <div class="m-auto lg:w-1/3">
        <h2>25% GENESIS COLLECTION</h2>
        <p>
          The Block God Generator is released and will enable the community to create their own
          Gods. The Gods created will be voted on by the community and minted. The creator gets 50%
          of the proceeds when their God is minted and sold.
        </p>
      </div>
    </div>
    <!-- Section 2 -->
    <div class="flex lg:flex-row flex-col space-x-10 py-10 px-10">
      <div class="m-auto lg:w-1/3 sec2Text">
        <h2>50% GENESIS COLLECTION</h2>
        <p>
          Voting on artists for the community who will design specific features of the Artverse will
          begin 100% Genesis Collection Sale - The building of the Artverse will begin. We will
          start with intimate conversations between designers/artists and the community. The
          community will play a continuous guiding role in the building of the Artverse.
        </p>
      </div>
      <img src="/images/uploads/roadmap_2-01.svg" alt="" class="svg-img lg:w-1/3" />
    </div>
    <!-- Section 3 -->
    <div class="flex lg:flex-row flex-col space-x-10 py-10 px-10">
      <img src="/images/uploads/roadmap-03.svg" alt="" class="svg-img lg:w-1/3" />
      <img src="/images/uploads/roadmap-04.svg" class="fancyDiv lg:w-1/3" alt="" />
      <div class="m-auto lg:w-1/3">
        <h2>100% GENESIS COLLECTION</h2>
        <p>
          The building of the Artverse will begin. We will start with intimate conversations between
          designers/artists and the community. The community will play a continuous guiding role in
          the building of the Artverse.
        </p>
      </div>
    </div>
    <!-- Section 4 -->
    <div class="flex lg:flex-row flex-col space-x-10 py-10 px-10">
      <div>
        <h2>Phase One Q3 (2022)</h2>
        <p>
          Limited explorable areas and unlimited shadow areas are made available in the Artverse and
          will eventually be populated with more terrains and life forms with time and as per
          community consensus.
        </p>
      </div>
      <div>
        <h2>Phase One Q3 (2023)</h2>
        <p>
          Communities will be able to build their own settlements and civilisations on the terrain
          by playing the Gods of Block Tactical Role Playing Game (TRPG).
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {};
</script>

<style>
@media (max-width: 800px) {
  .fancyDiv {
    display: none;
  }
  .svg-img {
    max-width: 100%;
    max-height: 100%;
    /* padding: 20px; */
  }
}

.svg-img {
  max-width: 35vw;
  padding: 20px;
}
.fancyDiv {
  max-height: 50vh;
  padding: 10px;
}
</style>
