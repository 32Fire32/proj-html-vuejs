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
  width: calc(var(--container) / 3 - 2.5rem);
  margin: var(--margin-small);
  position: relative;
  .hide {
    display: none;
    p:first-child {
      top: 65%;
    }
    p:last-child {
      font-size: 0.8rem;
    }
  }

  a {
    color: #fff;
    position: absolute;
    top: 1.25rem;
    right: 1.25rem;
  }
  img {
    width: 100%;
    border-radius: 0.625rem;
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

.card:hover img {
  filter: blur(0.125rem) brightness(40%);
}
.card:hover .hide {
  display: block;
}

.card:hover .show {
  display: none;
}
</style>
