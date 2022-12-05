<script>
import AppSection1 from "./sections/AppSection1.vue";
import AppSection2 from "./sections/AppSection2.vue";
import AppSection3 from "./sections/AppSection3.vue";
import AppSection4 from "./sections/AppSection4.vue";
import AppSection5 from "./sections/AppSection5.vue";
export default {
  name: "AppMain",
  components: {
    AppSection1,
    AppSection2,
    AppSection3,
    AppSection4,
    AppSection5,
  },
};
</script>

<template>
  <AppSection1 />
  <AppSection2 />
  <AppSection3 />
  <AppSection4 />
  <AppSection5 />
</template>

<style scoped lang="scss"></style>
