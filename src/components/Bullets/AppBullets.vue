<script>
export default {
  name: "AppBullets",
};
</script>

<template>
  <div class="bullets">
    <img src="../../assets/bullets.png" alt="bullets" />
  </div>
</template>

<style scoped lang="scss">
.bullets {
  width: 7.5rem;
  height: 3.4375rem;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: opacity(50%);
  }
}
</style>
