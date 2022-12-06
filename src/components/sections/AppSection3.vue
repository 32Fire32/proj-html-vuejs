<script>
import AppCards3 from "./SectionCards/AppCards3.vue";
export default {
  name: "AppSection3",
  components: {
    AppCards3,
  },
  data() {
    return {
      links: [
        "ALL",
        "INSTITUTIONAL",
        "SOCIAL",
        "EVENTS",
        "INNOVATION",
        "ENVIRONMENT",
        "TECHNOLOGY",
      ],
      cards: [
        {
          idsrc: "1",
          title: "Academic professional program in social media",
        },
        {
          idsrc: "2",
          title: "President's speech at the annual meeting",
        },
        {
          idsrc: "3",
          title: "International business trip in Shanghai",
        },
        {
          idsrc: "4",
          title: "Technology workshop with education theme",
        },
        {
          idsrc: "5",
          title: "Donation of clothes and food to the partner NGO",
        },
        {
          idsrc: "6",
          title: "Confraternization of the procurement team",
        },
      ],
    };
  },
};
</script>

<template>
  <section>
    <div class="container">
      <div class="introSection">
        <span>WE DO MORE FOR EVERYONE</span>
      </div>
      <div class="titleSection center-align">
        <h2 class="firstAbout">Actions &</h2>
        <h2 class="second">Projects</h2>
      </div>
      <nav class="light-text">
        <div v-for="link in links">
          <a href="#">{{ link }}</a>
        </div>
      </nav>
      <div class="cards">
        <div v-for="card in cards">
          <AppCards3 :img="card.idsrc" :title="card.title" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  .introSection {
    margin-top: var(--margin-big);
    margin-bottom: var(--margin-small);
  }
  .cards {
    display: flex;
    flex-wrap: wrap;
    margin-bottom: var(--margin-big);
  }
  .titleSection h2 {
    font-size: 3.5rem;
    margin-bottom: var(--margin);
  }
  nav {
    display: flex;
    justify-content: space-between;
    margin-bottom: var(--margin);
    width: 70%;

    a {
      text-decoration: none;
      color: var(--text-color-light);
    }
  }
}
</style>
