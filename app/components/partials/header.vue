<template>
  <header class="flex items-center py-4 md:py-8 headboi">
    <!-- <header> -->
    <!-- <label for="navbar-toggle"><i></i></label> -->
    <div class="header__logo">
      <nuxt-link to="/">
        <img :src="logo" alt="Logo" />
      </nuxt-link>
    </div>

    <!-- <input type="checkbox" id="navbar-toggle" /> -->
    <!-- <label for="navbar-toggle"><i></i></label> -->
    <nav class="nav ml-auto" id="mainNav">
      <!-- eslint-disable-next-line vue-a11y/form-has-label -->
      <input type="checkbox" id="nav-check" />
      <div class="nav-btn">
        <label for="nav-check">
          <i></i>
          <!-- <span></span>
          <span></span>
          <span></span> -->
        </label>
      </div>
      <!-- <nav class="menu"> -->
      <!-- <button
        @click="toggleMenuOpen()"
        @keydown="toggleMenuOpen()"
        class="
          flex
          items-center
          px-3
          py-2
          border
          rounded
          text-teal-200
          border-teal-400
          hover:text-white hover:border-white
        "
      >
        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
      </button> -->
      <ul
        class="flex md:flex-row flex-col sm:mt-4 sm:pt-4 md:mt-0 md:pt-0 md:mr-4 lg:mr-0 nav-links"
      >
        <!-- <ul class="nav-links"> -->
        <!-- <li>
          <nuxt-link to="/blog" class="block font-medium px-4 py-1 md:p-2 lg:px-4">
            Blog
          </nuxt-link>
        </li> -->

        <!-- <li
          v-for="(page, index) in pages"
          :key="index"
          class="block font-medium px-4 py-1 md:p-2 lg:px-4"
        >
          <nuxt-link :to="`/${page.slug}`">{{ page.title }}</nuxt-link>
        </li> -->
        <li class="block font-medium px-4 py-1 md:p-2 lg:px-4">
          <nuxt-link to="/site" @click.native="menuClicked" @keydown="menuClicked">
            About Us
          </nuxt-link>
        </li>
        <li class="block font-medium px-4 py-1 md:p-2 lg:px-4">
          <nuxt-link to="/team" @click.native="menuClicked" @keydown="menuClicked">
            Team
          </nuxt-link>
        </li>
        <li class="block font-medium px-4 py-1 md:p-2 lg:px-4">
          <nuxt-link to="/gallery" @click.native="menuClicked" @keydown="menuClicked">
            Gallery
          </nuxt-link>
        </li>
        <li class="block font-medium px-4 py-1 md:p-2 lg:px-4">
          <nuxt-link to="/roadmap" @click.native="menuClicked" @keydown="menuClicked">
            RoadMap
          </nuxt-link>
        </li>
        <li class="block font-medium px-4 py-1 md:p-2 lg:px-4" id="discordBtn">
          <a href="https://discord.gg/FRnchPtbgP" target="_blank">
            <svg
              id="discordIcon"
              data-name="Layer 1"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 30 30"
            >
              <path
                d="M28.3,17.28a29.09,29.09,0,0,0-2-7.66,6.19,6.19,0,0,0-3.65-3.56,10,10,0,0,0-4.06-.82c0,.7,0,.7.62.83a5.87,5.87,0,0,1,3.18,1.5A18.55,18.55,0,0,0,7.51,7.44a24.13,24.13,0,0,1,3.3-1.36c.45-.15.83-.24.48-.9-.55.07-1.13.12-1.69.21-3.17.54-5.44,2.17-6.38,5.37a1.33,1.33,0,0,1-.1.28,35.07,35.07,0,0,0-1.71,9.79,1.49,1.49,0,0,0,.3.94,8.64,8.64,0,0,0,5.25,3,2.58,2.58,0,0,0,1.72-.12,8.3,8.3,0,0,0,1.44-1.94l-3-1.59a19.38,19.38,0,0,0,15.7,0l-3,1.56c.35.52.73,1,1,1.55a1.18,1.18,0,0,0,1.25.6,8.63,8.63,0,0,0,6-2.9,1.6,1.6,0,0,0,.41-1C28.55,19.67,28.45,18.47,28.3,17.28ZM10.8,18.63a2.35,2.35,0,0,1,0-4.7A2.32,2.32,0,0,1,13,16.3,2.35,2.35,0,0,1,10.8,18.63Zm8.45,0a2.35,2.35,0,0,1-.05-4.7,2.31,2.31,0,0,1,2.23,2.36A2.34,2.34,0,0,1,19.25,18.63Z"
              /></svg
          ></a>
        </li>
        <li class="block font-medium px-4 py-1 md:p-2 lg:px-4" id="twitterBtn">
          <a href="https://twitter.com/godsofblock" target="_blank"
            ><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 30 30">
              <g style="isolation: isolate">
                <g id="b7942413-219f-469b-89ee-4d4b28af2835" data-name="Layer 1">
                  <g style="opacity: 0.5; mix-blend-mode: multiply">
                    <path
                      d="M1.41,23.68a11.75,11.75,0,0,0,5.84-1,10,10,0,0,0,2.34-1.39,5.65,5.65,0,0,1-2.4-.62,5.59,5.59,0,0,1-2.69-3c-.13-.32-.13-.32.22-.29a4.68,4.68,0,0,0,2.06-.14,8.23,8.23,0,0,1-1.35-.5,5.68,5.68,0,0,1-3-4.78c0-.26,0-.28.27-.17a5,5,0,0,0,2.21.57,11.81,11.81,0,0,1-1-.85,5.72,5.72,0,0,1-.87-6.35c.13-.27.19-.27.4,0a15.85,15.85,0,0,0,9.75,5.44c.42.06.84.09,1.27.15.26.05.3-.09.26-.31a5.62,5.62,0,0,1,9.4-5,.54.54,0,0,0,.6.14,11.11,11.11,0,0,0,3-1.16,1,1,0,0,0,.23-.13,5.8,5.8,0,0,1-2.37,3.09,11.38,11.38,0,0,0,3-.8.45.45,0,0,1-.13.32,12.16,12.16,0,0,1-2.32,2.38.48.48,0,0,0-.23.46,16.18,16.18,0,0,1-3.89,11,14.84,14.84,0,0,1-9.34,5.25A16.09,16.09,0,0,1,1.53,23.75.31.31,0,0,0,1.41,23.68Z"
                      style="fill: #676767; fill-rule: evenodd"
                    />
                  </g>
                  <path
                    d="M1.41,23.68a11.75,11.75,0,0,0,5.84-1,10,10,0,0,0,2.34-1.39,5.65,5.65,0,0,1-2.4-.62,5.59,5.59,0,0,1-2.69-3c-.13-.32-.13-.32.22-.29a4.68,4.68,0,0,0,2.06-.14,8.23,8.23,0,0,1-1.35-.5,5.68,5.68,0,0,1-3-4.78c0-.26,0-.28.27-.17a5,5,0,0,0,2.21.57,11.81,11.81,0,0,1-1-.85,5.72,5.72,0,0,1-.87-6.35c.13-.27.19-.27.4,0a15.85,15.85,0,0,0,9.75,5.44c.42.06.84.09,1.27.15.26.05.3-.09.26-.31a5.62,5.62,0,0,1,9.4-5,.54.54,0,0,0,.6.14,11.11,11.11,0,0,0,3-1.16,1,1,0,0,0,.23-.13,5.8,5.8,0,0,1-2.37,3.09,11.38,11.38,0,0,0,3-.8.45.45,0,0,1-.13.32,12.16,12.16,0,0,1-2.32,2.38.48.48,0,0,0-.23.46,16.18,16.18,0,0,1-3.89,11,14.84,14.84,0,0,1-9.34,5.25A16.09,16.09,0,0,1,1.53,23.75.31.31,0,0,0,1.41,23.68Z"
                    style="fill: #fdfeff; fill-rule: evenodd"
                  />
                </g>
              </g></svg
          ></a>
        </li>
      </ul>
    </nav>

    <!-- eslint-disable-next-line vue-a11y/click-events-have-key-events -->
    <!-- <button class="fixed bottom-0" @click="scrollo">TOP</button> -->
  </header>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component
export default class Header extends Vue {
  get pages(): Page[] {
    return this.$store.state.pages;
  }

  public scrollo(): void {
    // const nav = document.getElementById('mainNav');
    // console.log('srolltotop');
    // if (nav) {
    //   nav.scrollIntoView();
    // }
    document.body.scrollTop = 0; // For Safari
    document.documentElement.scrollTop = 0; // For Chrome, Firefox, IE and Opera
  }

  logo = settings.logo;

  isNavOpen = false;

  menuClicked(): void {
    const menuBtn = document.getElementById('nav-check');
    if (menuBtn) {
      menuBtn.click();
    }
  }
}
</script>

<style lang="scss">
.nav {
  ul li > a {
    &.nuxt-link-active {
      color: #fdb515;
      @apply font-bold;
    }
  }
}

.header__logo {
  max-width: 128px;
}
// NAVBAR CSS
.headboi {
  z-index: 9999;
}
.nav > .nav-btn {
  display: none;
}

.nav > .nav-links > .nuxt-link:hover {
  background-color: rgba(1, 1, 1, 0.3);
}

.nav > #nav-check {
  display: none;
}

// NAVBAR ANIMATION
.nav-btn label {
  user-select: none;
  cursor: pointer;
  padding: 30px 20px;
  position: relative;
  z-index: 3;
}

.nav-btn label i {
  height: 2px;
  position: relative;
  top: 12px;
  right: 2px;
  transition: background 0.2s ease-out;
  width: 28px;
  font-style: normal;
  font-weight: normal;
}
.nav-btn label i:before,
.nav-btn label i:after {
  content: '';
  height: 100%;
  position: absolute;
  transition: all 0.2s ease-out;
  width: 100%;
}
.nav-btn label i,
.nav-btn label i:before,
.nav-btn label i:after {
  display: block;
  background: #eee;
}
.nav-btn label i:before {
  top: 5px;
}
.nav-btn label i:after {
  top: -5px;
}

#nav-check:checked ~ .nav-btn label {
  background: #212121;
  border-radius: 50%;
}
#nav-check:checked ~ .nav-btn label i {
  background: transparent;
}
#nav-check:checked ~ .nav-btn label i:before {
  transform: rotate(-45deg);
}
#nav-check:checked ~ .nav-btn label i:after {
  transform: rotate(45deg);
}
#nav-check:checked ~ .nav-btn label:not(.steps) i:before,
#nav-check:checked ~ .nav-btn label:not(.steps) i:after {
  top: 0;
}
@media (max-width: 800px) {
  .nav > .nav-btn {
    display: inline-block;
    position: absolute;
    right: 10px;
    top: 10px;
  }
  .nav > .nav-btn > label {
    display: inline-block;
    width: 50px;
    height: 50px;
    padding: 13px;
  }

  .nav > .nav-links {
    position: absolute;
    display: block;
    width: 100%;
    background-color: rgba(1, 1, 1, 0.85);
    z-index: 100;
    backdrop-filter: blur(10px);
    height: 0px;
    transition: all 0.3s ease-in;
    overflow-y: hidden;
    top: 80px;
    left: 0px;
  }
  .nav > .nav-links > nuxt-link {
    display: block;
    width: 100%;
    padding: 10px;
  }
  .nav > #nav-check:not(:checked) ~ .nav-links {
    height: 0px;
  }
  .nav > #nav-check:checked ~ .nav-links {
    height: 30vh;
    overflow-y: auto;
  }
}

#discordIcon {
  width: 32px;
  fill: white;
  transition: 0.25s;
}
#discordIcon:hover {
  transition: 0.5s;
  // fill: #fdb515;
  // width: 50px;
}
#discordBtn {
  // background: #fdb515;
  // border-radius: 50%;
}

#twitterBtn a svg {
  width: 32px;
}
</style>
