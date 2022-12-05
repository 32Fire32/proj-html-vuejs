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
    <div class="top">
      <img :src="`src/assets/svg-${img}.svg`" :alt="title" />
      <div class="btncard">
        <button><i class="fa-sharp fa-solid fa-arrow-right"></i></button>
      </div>
    </div>
    <div class="bottom">
      <h4>{{ title }}</h4>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card {
  width: calc(var(--container) / 3 - 40px);
  background-color: #fff;
  padding: 30px;
  margin: 20px;
  border-radius: 10px;
  .top {
    display: flex;
    justify-content: space-between;
    .btncard {
      text-align: center;
      line-height: 1px;
      button {
        border: none;
        color: var(--primary-color);
        background-color: transparent;
        .fa-arrow-right:hover {
          background-color: #d5e7e8;
          color: var(--secondary-color);
          border-radius: 100%;
          cursor: pointer;
        }
      }
    }
    img {
      width: 50px;
    }
    .fa-arrow-right {
      font-size: 1.2rem;
    }
  }
  .bottom h4 {
    margin-top: 20px;
    margin-bottom: 20px;
  }
}
</style>
