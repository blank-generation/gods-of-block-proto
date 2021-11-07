<template>
  <div class="flex md:flex-row flex-col gap-x-10">
    <div class="md:w-1/2 mx-auto md:mx-0">
      <h1 class="text-center title">TEAM</h1>
      <img src="/images/uploads/teamill-01.svg" alt="" />
      <p>
        Indian political cartoonist Psycopomp has been involved in building art communities in
        various Indian cities for over a decade. Through a Fulbright Scholarship to study community
        art, Psycopomp was able to formulate these ideas and experiences to create a proposal for
        building such communities on a global scale. This vision attracted a small group of artists,
        thinkers, shamans and sorcerers of the cryptoverse. Before long it took shape as the project
        we now present to you as Gods of Block (GOB).
      </p>
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
          <p>SCRIBE, SHILLER-IN-CHIEF</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {};
</script>

<style>
.teamCont {
  background-image: url('/images/uploads/coming_soon_bg-01.svg');
  background-size: cover;
  background-position-x: center;
  /* height: 100vh; */
  font-size: 24px;
}

.teamboi {
  @apply flex gap-x-5;
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
