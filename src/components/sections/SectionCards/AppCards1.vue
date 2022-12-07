<script>
export default {
  name: "AppCards1",
  props: {
    title: String,
    img: String,
  },
};
</script>

<template>
  <div class="card">
    <div class="tb-padding">
      <div class="top center-align">
        <img :src="`src/assets/svg-${img}.svg`" :alt="title" />
        <div class="btncard">
          <button><i class="fa-sharp fa-solid fa-arrow-right"></i></button>
        </div>
      </div>
      <div class="bottom">
        <h3>{{ title }}</h3>
        <p class="light-text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card {
  width: calc(var(--container) / 3 - 2.5rem);
  background-color: #fff;
  border-radius: 0.625rem;
  padding: 1.875rem;
  margin: 1.25rem 0;
  .top {
    justify-content: space-between;
    .btncard {
      text-align: center;
      line-height: 0.0625rem;
      button {
        border: none;
        color: var(--text-bg-title-lightgreen);
        background-color: transparent;
        i {
          font-size: 1.5rem;
          padding: 0.625rem;
        }
        i:hover {
          background-color: #d5e7e8;
          color: var(--primary-color);
          border-radius: 100%;
          padding: 0.625rem;
          cursor: pointer;
        }
      }
    }
    img {
      width: 3.125rem;
    }
    .fa-arrow-right {
      font-size: 1.2rem;
    }
  }
  .bottom {
    width: 80%;
  }
  .bottom h3 {
    margin-top: var(--margin-small);
    margin-bottom: var(--margin-small);
    font-size: 1.6rem;
  }
}
</style>
