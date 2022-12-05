<script>
export default {
  name: "AppCards2",
  props: {
    title: String,
    img: String,
  },
};
</script>

<template>
  <div class="card">
    <div class="top">
      <span><i :class="img"></i></span>
      <h4>{{ title }}</h4>
    </div>
    <p class="light-text">
      Lorem ipsum dolor sit amet consectetur adipisicing elit.
    </p>
  </div>
</template>

<style scoped lang="scss">
.card {
  width: calc(var(--container) / 4 - 40px);
  color: #fff;
  margin: 20px;
  i {
    color: var(--primary-color);
  }
  p {
    color: var(--text-color-light);
  }
  .top {
    display: flex;
    align-items: center;
    span {
      font-size: 1.3rem;
    }
    img {
      width: 50px;
    }
    .fa-arrow-right {
      font-size: 1.2rem;
    }
  }
  .top h4 {
    color: #fff;
    font-size: 1.6rem;
    margin-top: 20px;
    margin-bottom: 20px;
    margin-left: 10px;
  }
}
</style>
