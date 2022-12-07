<script>
export default {
  name: "AppBackground",
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
    v-for="n in 10"
  ></div>
  <div
    class="square small"
    :style="{
      top: `${getRandomNumber(0, 100)}%`,
      left: `${getRandomNumber(0, 100)}%`,
    }"
    v-for="n in 10"
  ></div>
  <div
    class="square big"
    :style="{
      top: `${getRandomNumber(0, 100)}%`,
      left: `${getRandomNumber(0, 100)}%`,
    }"
    v-for="n in 10"
  ></div>
</template>

<style scoped lang="scss">
.square {
  position: absolute;
  z-index: -1;
  width: 6.25rem;
  height: 6.25rem;
  background-color: rgb(228, 228, 228);
  opacity: 0.5;
}
.small {
  width: 4.375rem;
  height: 4.375rem;
}
.big {
  width: 9.375rem;
  height: 9.375rem;
}
</style>
