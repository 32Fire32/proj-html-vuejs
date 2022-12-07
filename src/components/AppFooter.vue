<script>
import AppCardsFooter from "./sections/SectionCards/AppCardsFooter.vue";

export default {
  name: "AppFooter",
  components: {
    AppCardsFooter,
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
          <!-- cycle links -->
          <div class="card" v-for="card in cards">
            <AppCardsFooter :title="card.title" :link="card.links" />
          </div>
        </div>
      </div>
    </div>
    <!-- postfooter -->
    <div class="postfooter">
      <div class="container wrapper light-text">
        <span>Enjoy the price. We are tracking any intention of piracy</span>
        <span
          >© 2020 NEXGEN is Proudly Powered by
          <span class="green">Codings</span>.</span
        >
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
footer {
  .bg {
    background-color: var(--secondary-color);
    padding-top: var(--margin-big);
    padding-bottom: var(--margin-big);
  }

  .row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .card {
      width: calc(var(--container) / 4 - 1.25rem);
      .infos {
        margin: 0.625rem 0;
        color: --text-color-light;
        display: flex;
        flex-direction: column;

        .fa-solid {
          margin-right: 0.625rem;
          margin: 0.625rem 0;
        }
      }
      img {
        width: 50%;
        margin-bottom: 0.625rem;
      }
    }
    .btn-dark {
      background-color: var(--secondary-color);
    }
    .btn-dark:hover {
      background-color: var(--primary-color);
      color: #fff;
      border: none;
      padding: 0.625rem 1.25rem;
      border-radius: 0.125rem;
      cursor: pointer;
      border: 1px solid var(--primary-color);
    }
  }

  // postfooter
  .postfooter {
    background-color: black;
    .wrapper {
      padding: 2.5rem 0;
      color: var(--text-color-light);
      display: flex;
      justify-content: space-between;
      .green {
        color: var(--primary-color);
      }
    }
  }
}
</style>
