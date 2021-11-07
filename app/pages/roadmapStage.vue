<template>
  <div>
    <h2 class="text-center title">Roadmap</h2>

    <div class="timlineCont">
      <div class="timeline-block timeline-block-right">
        <div class="marker"></div>
        <div class="timeline-content">
          <h2>25% GENESIS COLLECTION</h2>
          <img src="/images/uploads/25p-01.svg" alt="" class="svg-img" />
          <p>
            The Block God Generator is released and will enable the community to create their own
            Gods. The Gods created will be voted on by the community and minted. The creator gets
            50% of the proceeds when their God is minted and sold.
          </p>
        </div>
      </div>

      <div class="timeline-block timeline-block-left">
        <div class="marker"></div>
        <div class="timeline-content">
          <h2>50% GENESIS COLLECTION</h2>
          <img src="/images/uploads/50PERC2-01.svg" alt="" class="svg-img" />
          <p>
            Voting on artists for the community who will design specific features of the Artverse
            will begin 100% Genesis Collection Sale - The building of the Artverse will begin. We
            will start with intimate conversations between designers/artists and the community. The
            community will play a continuous guiding role in the building of the Artverse.
          </p>
        </div>
      </div>

      <div class="timeline-block timeline-block-right">
        <div class="marker"></div>
        <div class="timeline-content">
          <h2>100% GENESIS COLLECTION</h2>
          <img src="/images/uploads/100PERC-01.svg" alt="" class="svg-img" />
          <p>
            The building of the Artverse will begin. We will start with intimate conversations
            between designers/artists and the community. The community will play a continuous
            guiding role in the building of the Artverse.
          </p>
        </div>
      </div>
    </div>
    <div
      class="
        flex
        md:flex-row
        flex-col
        md:space-x-20 md:space-y-0
        space-y-5
        justify-items-center justify-center
        phases
      "
    >
      <div class="md:w-1/3">
        <h2>PHASE ONE Q3 (2022)</h2>
        <p>
          Limited explorable areas and unlimited shadow areas are made available in the Artverse and
          will eventually be populated with more terrains and life forms with time and as per
          community consensus.
        </p>
      </div>
      <div class="md:w-1/3">
        <h2>PHASE TWO Q3 (2023)</h2>
        <p>
          Communities will be able to build their own settlements and civilisations on the terrain
          by playing the Gods of Block Tactical Role Playing Game (TRPG).
        </p>
      </div>
    </div>
  </div>
</template>

<style>
.timlineCont {
  width: 80%;
  padding: 50px 0;
  margin: 50px auto;
  position: relative;
  overflow: hidden;
}

.timeline-content h2,
.phases h2 {
  color: #f8b318;
}

.timlineCont:before {
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  margin-left: -1px;
  width: 2px;
  height: 100%;
  background: #ccd1d9;
  z-index: 1;
}

.timeline-block {
  width: -webkit-calc(50% + 8px);
  width: -moz-calc(50% + 8px);
  width: calc(50% + 8px);
  display: -webkit-box;
  display: -webkit-flex;
  display: -moz-box;
  display: flex;
  -webkit-box-pack: justify;
  -webkit-justify-content: space-between;
  -moz-box-pack: justify;
  justify-content: space-between;
  clear: both;
}

.timeline-block-right {
  float: right;
}

.timeline-block-left {
  float: left;
  direction: rtl;
}

.marker {
  width: 16px;
  height: 16px;
  transform: scale(4);
  background: url('/images/uploads/roadmap_bllock-01.svg');
  margin-top: 10px;
  z-index: 9999;
}

.timeline-content {
  width: 95%;
  padding: 0 15px;
  /* color: #666; */
}

@media screen and (max-width: 768px) {
  .timlineCont:before {
    left: 8px;
    width: 2px;
  }
  .timeline-block {
    width: 100%;
    margin-bottom: 30px;
  }
  .timeline-block-right {
    float: none;
  }

  .timeline-block-left {
    float: none;
    direction: ltr;
  }
}
</style>
