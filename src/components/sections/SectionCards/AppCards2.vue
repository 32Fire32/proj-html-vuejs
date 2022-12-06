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
  width: calc(var(--container) / 4 - 0.625rem);
  color: #fff;
  margin: 1.25rem 0rem;
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
      width: 3.125rem;
    }
    .fa-arrow-right {
      font-size: 1.2rem;
    }
  }
  .top h4 {
    color: #fff;
    font-size: 1.6rem;
    margin-top: var(--margin-small);
    margin-bottom: var(--margin-small);
    margin-left: 0.625rem;
  }
}
</style>
