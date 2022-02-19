<template>
  <div class="flex md:flex-row flex-col gap-x-10">
    <div class="md:w-2/3 mx-auto md:mx-0 md:flex-col flex-col-reverse flex">
      <!-- <h1 class="text-center title">TEAM</h1> -->
      <p class="md:px-16 px-2 md:pt-10 md:pb-0 pb-10 text-center">
        Indian political cartoonist Psycopomp has been involved in building art communities in
        various Indian cities for over a decade. Through a Fulbright Scholarship to study community
        art, Psycopomp was able to formulate these ideas and experiences to create a proposal for
        building such communities on a global scale. This vision attracted a small group of artists,
        thinkers, shamans and sorcerers of the cryptoverse. Before long it took shape as the project
        we now present to you as Gods of Block (GOB).
      </p>
      <img src="/images/uploads/teamill-01.svg" alt="" />
    </div>
    <div class="flex flex-col">
      <!-- Satiwik -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/satwik-01.svg" alt="" />
        <div class="my-auto">
          <h2>PSYCOPOMP</h2>
          <p>ARTMONGER, FOUNDER</p>
        </div>
      </div>
      <!-- Gulla0 -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/harsha-01.svg" alt="" />
        <div class="my-auto">
          <h2>GULLA0</h2>
          <p>ADA NATIVE, COMMUNITY SHAMAN</p>
        </div>
      </div>
      <!-- Srini -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/srini-01.svg" alt="" />
        <div class="my-auto">
          <h2>PERFECTSYSTEM<br />IAMFALLING</h2>
          <p>TECHSMITH, NERD</p>
        </div>
      </div>
      <!-- Kota -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/kota-01.svg" alt="" />
        <div class="my-auto">
          <h2>HAKUNAKOTATA</h2>
          <p>ART-ALCHEMIST, GAMER</p>
        </div>
      </div>
      <!-- Vijay -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/vijay-01.svg" alt="" />
        <div class="my-auto">
          <h2>BUZZEDART</h2>
          <p>SCRIBE, <br />SHILLER-IN-CHIEF</p>
        </div>
      </div>
      <!-- Sam -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/sam.png" alt="" />
        <div class="my-auto">
          <h2>CARDAPPER</h2>
          <p>PLUTUS PROGRAMMER, <br />BOY WONDER</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {};
</script>

<style>
.teamboi {
  @apply flex gap-x-5 my-3;
}

.teamboi img {
  /* @apply mx-auto; */
  max-width: 128px;
}

.teamboi h2 {
  font-size: 18px;
}

@media (max-width: 800px) {
  .teamboi img {
    @apply mx-auto;
  }
  .teamboi {
    @apply my-5;
  }
  .teamboi .my-auto {
    @apply text-center;
  }
}
</style>
