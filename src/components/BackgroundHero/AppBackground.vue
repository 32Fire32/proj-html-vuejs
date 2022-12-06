<script>
export default {
  name: "AppBackground",
  //   data() {
  //     return {
  //       top: 0,
  //       left: 0,
  //     };
  //   },
  methods: {
    getRandomNumber(min, max) {
      return Math.random() * (max - min) + min;
    },
  },
};
</script>

<template>
  <div
    class="square"
    :style="{
      top: `${getRandomNumber(0, 100)}%`,
      left: `${getRandomNumber(0, 100)}%`,
    }"
    v-for="n in 20"
  ></div>
</template>

<style scoped lang="scss">
.square {
  position: absolute;
  z-index: -1;
  width: 100px;
  height: 100px;
  background-color: rgb(228, 228, 228);
  opacity: 0.5;
}
</style>
