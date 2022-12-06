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
    <a href="" class="hide"><i class="fa-solid fa-arrow-right"></i></a>
    <p class="show">
      <strong>{{ title }}</strong>
    </p>
    <div class="hide">
      <p>
        <strong>{{ title }}</strong>
      </p>
      <p class="light-text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
      </p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card {
  width: calc(var(--container) / 3 - 40px);
  margin: 20px;
  position: relative;
  a {
    text-decoration: none;
    color: #fff;
    position: absolute;
    top: 20px;
    right: 20px;
  }
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
  font-size: 1.2rem;
}
.hide {
  display: none;
  p:first-child {
    top: 65%;
  }
  p:last-child {
    font-size: 0.8rem;
  }
}

.card:hover {
  cursor: pointer;
}

.card:hover img {
  filter: blur(2px) brightness(40%);
}
.card:hover .hide {
  display: block;
}

.card:hover .show {
  display: none;
}
</style>
