<script>
import AppSection1 from "./sections/AppSection1.vue";
import AppSection2 from "./sections/AppSection2.vue";
import AppSection3 from "./sections/AppSection3.vue";
import AppSection4 from "./sections/AppSection4.vue";
import AppSection5 from "./sections/AppSection5.vue";
import AppBullets from "./Bullets/AppBullets.vue";
export default {
  name: "AppMain",
  components: {
    AppSection1,
    AppSection2,
    AppSection3,
    AppSection4,
    AppSection5,
    AppBullets,
  },
};
</script>

<template>
  <AppSection1 />
  <!-- componenti bullet in posizione assoluta -->
  <div class="relative">
    <div class="top">
      <AppBullets />
    </div>
    <AppSection2 />
    <div class="bottom">
      <AppBullets />
    </div>
  </div>
  <AppSection3 />
  <AppSection4 />
  <AppSection5 />
</template>

<style scoped lang="scss">
.relative {
  position: relative;
  .top {
    position: absolute;
    z-index: 20;
    top: -1.875rem;
    left: calc(50% - 3.75rem);
  }
  .bottom {
    position: absolute;
    bottom: -1.5625rem;
    left: calc(50% - 60px);
  }
}
</style>
