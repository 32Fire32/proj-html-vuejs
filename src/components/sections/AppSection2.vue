<script>
import AppCards2 from "./SectionCards/AppCards2.vue";
export default {
  name: "AppSection2",
  components: {
    AppCards2,
  },

  data() {
    return {
      cards: [
        {
          src: "fa-solid fa-medal",
          title: "Tradition",
        },
        {
          src: "fa-sharp fa-solid fa-shield",
          title: "Security",
        },
        {
          src: "fa-regular fa-pen-to-square",
          title: "Certificate",
        },
        {
          src: "fa-solid fa-graduation-cap",
          title: "Expertise",
        },
      ],
    };
  },
};
</script>

<template>
  <section>
    <div class="container">
      <div class="text">
        <span class="introSection">ABOUT THE NETWORK</span>
        <div class="titleSection center-align">
          <h2 class="firstAbout">The</h2>
          <h2>Company</h2>
        </div>
        <div class="sloganSection center-align">
          <div class="text">
            <p>
              For 12 years we have been providing audit and warranty, financial
              advice, risk advice, taxes and related services to selcet clients.
            </p>
          </div>
        </div>
        <div class="cards">
          <div v-for="card in cards">
            <AppCards2 :img="card.src" :title="card.title" />
          </div>
        </div>
        <div class="buttons">
          <button class="btn">GET IN TOUCH</button>
          <button class="btn-light">READ MORE</button>
        </div>
      </div>
      <div class="image"></div>
    </div>
  </section>
</template>

<style scoped lang="scss">
section {
  background-color: black;
  background-image: url(../../assets/about-4.jpg);
  background-repeat: no-repeat;
  background-position: right top;

  .titleSection {
    color: #fff;
    margin-bottom: 20px;
    .firstAbout {
      background-color: var(--primary-color);
      padding: 5px;
      margin-right: 5px;
    }
  }
  .text {
    width: 50%;
    display: flex;
    flex-direction: column;
    .introSection {
      margin-top: 80px;
      margin-bottom: 20px;
      color: var(--primary-color);
    }
    p {
      color: var(--text-color-light);
      margin-bottom: var(--margin-bottom);
    }
    .buttons {
      margin-bottom: 80px;
    }
  }
  .image {
    width: 50%;
  }
}
.cards {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: var(--margin-bottom);
}
</style>
