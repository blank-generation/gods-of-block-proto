<template>
  <div>
    <h1 class="text-center">Roadmap</h1>

    <div class="timlineCont">
      <div class="timeline-block timeline-block-right">
        <div class="marker"></div>
        <div class="timeline-content">
          <div>
            <h2>25% GENESIS COLLECTION</h2>
            <img src="/images/uploads/25p-01.svg" alt="" class="svg-img" />
          </div>
          <div>
            <p>
              Launch of the first community led GOB initiative: The Cryptionary Project. The
              crowd-sourced cryptionary project ensures that new artists have a guiding tool that
              helps them make sense of the “meta-vernacular” which is slowly evolving into a dialect
              or even a language of its own. By sourcing important etymological and epistemological
              information about these words we enable academic research into the linguistics of the
              “meta-vernacular”. 100 GOB NFTs are reserved as giveaways for the highest
              contributors.
            </p>
          </div>
        </div>
      </div>

      <div class="timeline-block timeline-block-left">
        <div class="marker"></div>
        <div class="timeline-content">
          <h2>50% GENESIS COLLECTION</h2>
          <img src="/images/uploads/50perc-01.png" alt="" class="svg-img pt-10" />
          <p>
            Launch of community voting systems. Community voting systems are an exercise in meta
            democracy. The community will vote on what kind of voting systems work best for various
            important decision making processes. Voting on how to vote?! That’s some truly meta
            shit.
          </p>
        </div>
      </div>

      <div class="timeline-block timeline-block-right">
        <div class="marker"></div>
        <div class="timeline-content">
          <h2>100% GENESIS COLLECTION</h2>
          <img src="/images/uploads/100PERC-01.svg" alt="" class="svg-img pt-10" />
          <p>
            The Block God Generator is released and will enable the community to create their own
            Gods. The Gods created will be voted on by the community and minted. The creator gets
            50% of the proceeds when their God is minted and sold.
          </p>
        </div>
      </div>
    </div>
    <img src="/images/uploads/phase-01.svg" class="phaseImg" alt="" />
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
          The community will be able to build their own settlements and civilisations on the terrain
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
.timeline-block-left p {
  direction: ltr;
}
.timeline-block-left h2 {
  direction: ltr;
  text-align: right;
}

.marker {
  width: 16px;
  height: 16px;
  transform: scale(6);
  background: url('/images/uploads/roadmap_bllock-01.svg');
  margin-top: 10px;
  z-index: 99;
}

.timeline-content {
  width: 95%;
  padding: 0 15px;
  /* color: #666; */
}

.phaseImg {
  max-width: 800px;
  @apply mx-auto pb-10;
}
/* .timeline-content {
  display: flex;
  flex-direction: row-reverse;
} */
.timeline-content {
  /* @apply w-1/2 mx-auto; */
}
@media screen and (max-width: 768px) {
  .timlineCont:before {
    left: 12px;
    width: 2px;
  }
  .timlineCont {
    padding: 0px;
    margin: 0;
    width: 100%;
    margin-top: 40px;
  }

  .marker {
    /* width: 8px;
    height: 8px;
    transform: scale(6); */
    transform: scale(3.5);
    position: relative;
    left: 4px;
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

  .timeline-block-left h2 {
    direction: ltr;
    /* text-align: left; */
  }

  .timeline-block h2 {
    text-align: center;
  }
}
</style>
