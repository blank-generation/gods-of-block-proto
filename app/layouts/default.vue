<template>
  <main :class="[$route.name]" class="main px-4 md:px-0">
    <div class="container mx-auto">
      <site-header />
      <nuxt class="nuxt" />
    </div>
    <site-footer class="my-20" />
  </main>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import SiteHeader from '@/components/partials/header.vue';
import SiteFooter from '@/components/partials/footer.vue';

@Component({
  components: {
    SiteHeader,
    SiteFooter,
  },
})
export default class DefaultLayout extends Vue {}
</script>

<style lang="scss">
.divider {
  position: relative;
  min-width: 100vw;
  margin-top: auto;
}

.nuxt {
  transition: all 0.5s cubic-bezier(0.55, 0, 0.1, 1);
}

.main {
  background: #1a1a1aff;
}
</style>
