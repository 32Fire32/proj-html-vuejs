<script>
import AppCards1 from "./SectionCards/AppCards1.vue";
export default {
  name: "AppSection1",
  components: {
    AppCards1,
  },
  data() {
    return {
      cards: [
        {
          idsrc: "1",
          title: "Audit & Assurance",
        },
        {
          idsrc: "2",
          title: "Financial Advisory",
        },
        {
          idsrc: "3",
          title: "Analytics and M&A",
        },
        {
          idsrc: "4",
          title: "Middle Marketing",
        },
        {
          idsrc: "5",
          title: "Legal Consulting",
        },
        {
          idsrc: "6",
          title: "Regulatory Risk",
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
        <span>OUR BUSINESS AREA</span>
      </div>
      <div class="titleSection">
        <h2 class="first">Excellence in</h2>
        <h2 class="second">Services</h2>
      </div>
      <div class="sloganSection center-align">
        <div class="text">
          <p>
            We are leaders in providing consultancy services with a set of
            cutting-edge technologies and a a team of experienced and renowed
            professionals. These are some options that you can hire
          </p>
        </div>
        <div class="see">
          <button class="btn">SEE ALL</button>
        </div>
      </div>
      <!-- card cycle -->
      <div class="cards">
        <div v-for="card in cards">
          <AppCards1 :img="card.idsrc" :title="card.title" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
section {
  padding-top: var(--padding-big);
  padding-bottom: var(--padding-big);
  background-color: #eef4ed;

  .titleSection {
    display: flex;
    h2 {
      font-size: 3.5rem;
    }
    .second {
      margin-left: 0.3125rem;
    }
  }
}
.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
p {
  margin-top: var(--margin-small);
  font-weight: 100;
  color: var(--text-color-light);
}
.sloganSection {
  justify-content: space-between;
  width: 100%;
  .btn:hover {
    color: var(--primary-color);
    background-color: #eef4ed;
    border: 1px solid var(--primary-color);
    padding: 0.625rem 1.25rem;
    border-radius: 0.125rem;
  }
  .text {
    width: 70%;
  }
}
</style>
