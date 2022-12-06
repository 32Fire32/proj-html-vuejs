<script>
import AppCardsFooter from "./sections/SectionCards/AppCardsFooter.vue";
import porco from "./sections/AppSection1.vue";

export default {
  name: "AppFooter",
  components: {
    AppCardsFooter,
    porco,
  },

  data() {
    return {
      cards: [
        {
          title: "About",
          links: [
            "The Company",
            "Institutional",
            "Social & Events",
            "Innovations",
            "Environment",
            "Technology",
          ],
        },
        {
          title: "Services",
          links: [
            "Audit & Assurance",
            "Financial Advisory",
            "Analytics M&A",
            "Middle Marketing",
            "Legal Consulting",
            "Regulatory Risk",
          ],
        },
        {
          title: "Support",
          links: [
            "Responsability",
            "Terms of Use",
            "About Cookies",
            "Privacy Policy",
            "Accessibility",
            "Information",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <footer>
    <div class="bg">
      <div class="container">
        <div class="row">
          <div class="card">
            <img src="../assets/logoinv.png" alt="logobl" />
            <p class="light-text t">
              A functional HTML Template for Corporate & Business.
            </p>
            <div class="infos light-text">
              <div class="phone">
                <span>
                  <i class="fa-solid fa-phone"></i> +1(305) 1234-5678
                </span>
              </div>
              <div class="mail">
                <span
                  ><i class="fa-solid fa-envelope"></i> hello@example.com</span
                >
              </div>
              <div class="position">
                <span
                  ><i class="fa-solid fa-location-dot"></i> Main Avenue,
                  987</span
                >
              </div>
            </div>
            <button class="btn-dark">GET IN TOUCH</button>
          </div>
          <div class="card" v-for="card in cards">
            <AppCardsFooter :title="card.title" :link="card.links" />
          </div>
        </div>
      </div>
    </div>
    <div class="postfooter">
      <div class="container wrapper">
        <span>Enjoy the proce. We are tracking any intention of piracy</span>
        <span
          >© 2020 NEXGEN is Proudly Powered by<span class="green">Codings</span
          >.</span
        >
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
footer {
  .bg {
    background-color: #111117;
    padding-top: var(--margin-big-top);
    padding-bottom: var(--margin-big-top);
  }

  .row {
    display: flex;
    justify-content: space-between;
    align-items: center;

    .card {
      width: calc(var(--container) / 4 - 20px);
      margin: 10px;
      img {
        width: 70%;
      }
    }
  }
  .postfooter {
    background-color: black;
    .wrapper {
      padding: 40px 0;
      color: var(--text-color-light);
      display: flex;
      justify-content: space-between;
      .green {
        color: var(--primary-color);
      }
    }
  }
}
.right {
  width: 30%;
  padding: 20px;
  .t {
    margin-bottom: 20px;
  }
  h3 {
    margin-bottom: 20px;
  }
}
.infos {
  margin: 10px 0;
  color: --text-color-light;
  display: flex;
  flex-direction: column;

  .fa-solid {
    margin-right: 10px;
    margin: 10px 0;
  }
}
</style>
