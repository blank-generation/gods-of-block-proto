<template>
  <div class="flex gap-x-5 flex-wrap gap-y-5 justify-center">
    <CoolLightBox :items="items" :index="index" @close="index = null" :effect="'fade'">
    </CoolLightBox>

    <img
      class="image"
      v-for="(image, imageIndex) in items"
      :key="imageIndex"
      @click="index = imageIndex"
      @keydown="index = imageIndex"
      :src="image.src"
      alt=""
    />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import CoolLightBox from 'vue-cool-lightbox';
import 'vue-cool-lightbox/dist/vue-cool-lightbox.min.css';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
  components: {
    // Landing,
    CoolLightBox,
  },
})
export default class Gallery extends Vue {
  items = [
    {
      title: 'Zeus',

      src: '/images/uploads/Zeus.gif',
    },
    {
      title: 'Balabhadra',

      src: '/images/uploads/Balabhadra.gif',
    },
    {
      title: 'Cleopatra',

      src: '/images/uploads/Cleopatra.gif',
    },
    {
      title: 'Garuda',

      src: '/images/uploads/Garuda.gif',
    },
    {
      title: 'Hadad',

      src: '/images/uploads/Hadad.gif',
    },
    {
      title: 'Indra',

      src: '/images/uploads/Indra.gif',
    },
    {
      title: 'Lakshmi',

      src: '/images/uploads/Lakshmi.gif',
    },

    {
      title: 'Parvati',

      src: '/images/uploads/Parvati.gif',
    },
    {
      title: 'Monke',

      src: '/images/uploads/Monke.gif',
    },
    {
      title: 'Punkchick',

      src: '/images/uploads/Punkchick.gif',
    },
    {
      title: 'Thor',

      src: '/images/uploads/Thor.gif',
    },
    {
      title: 'Set',

      src: '/images/uploads/Set.gif',
    },
  ];

  index = null;
}
</script>

<style>
.image {
  /* width: 100px;
  height: 100px; */
  max-height: 300px;
  /* height: auto; */
}
</style>
