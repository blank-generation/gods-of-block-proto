<template>
  <div class="flex md:flex-row flex-col gap-x-10">
    <div class="w-1/2 mx-auto md:mx-0">
      <img src="/images/uploads/teamill-01.svg" alt="" />
    </div>
    <div class="flex flex-col">
      <!-- Satiwik -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/satwik-01.svg" alt="" />
        <div class="my-auto">
          <h2>PSYCHOPOMP</h2>
          <p>ARTIST</p>
        </div>
      </div>
      <!-- Gulla0 -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/harsha-01.svg" alt="" />
        <div class="my-auto">
          <h2>GULLA0</h2>
          <p>ADA NATIVE</p>
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
          <p>ARTIST</p>
        </div>
      </div>
      <!-- Vijay -->
      <div class="teamboi flex md:flex-row flex-col">
        <img src="/images/uploads/vijay-01.svg" alt="" />
        <div class="my-auto">
          <h2>BUZZED_ART</h2>
          <p>ARTIST</p>
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
  font-size: 36px;
}

.teamboi {
  @apply flex gap-x-5;
}
</style>
