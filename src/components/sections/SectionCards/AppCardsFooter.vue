<script>
export default {
  name: "AppCardsFooter",
  props: {
    title: String,
    link: Array,
  },
};
</script>

<template>
  <div class="linknav">
    <div>
      <h3>{{ title }}</h3>
      <ul class="light-text">
        <li v-for="li in link">
          <i class="fa-solid fa-chevron-right"></i><a href="">{{ li }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped lang="scss">
.linknav {
  background-color: #19191f;
  padding: var(--padding-small);
  color: #fff;
  display: flex;
  justify-content: center;
  h3 {
    margin-bottom: var(--margin-small);
  }
  li {
    margin-bottom: 0.625rem;
    a {
      color: var(--text-color-light);
    }
    i {
      margin-right: 0.625rem;
    }
  }
}
</style>
