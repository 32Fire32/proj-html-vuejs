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
    <div class="container center-align">
      <div class="text">
        <div class="introSection">
          <span>ABOUT THE NETWORK</span>
        </div>
        <div class="titleSection center-align">
          <h2 class="firstAbout">The</h2>
          <h2>Company</h2>
        </div>
        <div class="sloganSection center-align">
          <div class="text">
            <p class="light-text">
              For 12 years we have been providing audit and warranty, financial
              advice, risk advice, taxes and related services to select clients.
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
          <button class="btn-dark">READ MORE</button>
        </div>
      </div>
      <div class="image">
        <img src="../../assets/about-4.jpg" alt="" />
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
section {
  background-color: var(--secondary-color);
  overflow-x: hidden;
  position: relative;
  .titleSection {
    color: #fff;
    margin-bottom: var(--margin);
    h2 {
      font-size: 3.5rem;
    }
    .firstAbout {
      background-color: var(--text-bg-title-green);
      padding: 0.3125rem 1.25rem;
      margin-right: 0.3125rem;
    }
  }
  .text {
    width: 50%;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    .cards {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      margin-bottom: var(--margin);
    }
    .introSection {
      margin-bottom: var(--margin-small);
      color: var(--primary-color);
    }
    p {
      margin-bottom: var(--margin-small);
    }
    .btn-dark {
      margin-left: var(--margin-small);
      background-color: var(--secondary-color);
      &:hover {
        background-color: var(--primary-color);
        cursor: pointer;
      }
    }
    .btn:hover {
      color: #fff;
      background-color: var(--secondary-color);
      border: 0.0625rem solid var(--primary-color);
      padding: 0.625rem 1.25rem;
      border-radius: 0.125rem;
    }
  }
  .image {
    width: 50%;
    img {
      display: block;
    }
  }
}
</style>
