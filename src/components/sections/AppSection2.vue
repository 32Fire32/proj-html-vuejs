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
        <span class="introSection">ABOUT THE NETWORK</span>
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
    margin-bottom: 20px;
    h2 {
      font-size: 4rem;
    }
    .firstAbout {
      background-color: var(--text-bg-title-green);
      padding: 5px 20px;
      margin-right: 5px;
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
      margin-bottom: var(--margin-bottom);
    }
    .introSection {
      margin-bottom: 20px;
      color: var(--primary-color);
    }
    p {
      margin-bottom: var(--margin-bottom);
    }
    .btn-dark {
      margin-left: 20px;
      background-color: #111117;
      &:hover {
        background-color: var(--primary-color);
        cursor: pointer;
      }
    }
    .btn:hover {
      color: #fff;
      background-color: var(--secondary-color);
      border: 1px solid var(--primary-color);
      padding: 10px 20px;
      border-radius: 2px;
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
