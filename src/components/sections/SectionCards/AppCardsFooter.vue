<script>
export default {
  name: "AppCardsFooter",
  props: {
    title: String,
    link: String,
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
  padding: 20px;
  color: #fff;
  display: flex;
  justify-content: center;
  h3 {
    margin-bottom: 20px;
  }
  ul {
    list-style: none;

    li {
      margin-bottom: 10px;
      a {
        text-decoration: none;
        color: var(--text-color-light);
      }

      i {
        margin-right: 10px;
      }
    }
  }
}
</style>
