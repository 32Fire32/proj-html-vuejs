<script>
export default {
  name: "AppCards3",
  props: {
    title: String,
    img: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="`src/assets/project-${img}.jpg`" :alt="title" />
    <p>
      {{ title }}
    </p>
  </div>
</template>

<style scoped lang="scss">
.card {
  width: calc(var(--container) / 3 - 40px);
  margin: 20px;
  position: relative;
  img {
    width: 100%;
    border-radius: 10px;
    filter: brightness(60%);
  }
}
p {
  text-align: center;
  position: absolute;
  top: 80%;
  left: 20%;
  transform: translate(-10%, -50%);
  color: #fff;
}
</style>
