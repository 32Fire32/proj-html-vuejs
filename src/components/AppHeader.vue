<script>
import AppBackground from "./BackgroundHero/AppBackground.vue";
export default {
  name: "AppHeader",
  components: {
    AppBackground,
  },
  data() {
    return {
      links: ["HOME", "SERVICE", "ABOUT", "PROJECTS", "RESULTS"],
    };
  },
};
</script>

<template>
  <header>
    <div class="bgc">
      <!-- preheader -->
      <div class="container">
        <div class="preHeader">
          <div class="openhours">
            <span
              ><i class="fa-solid fa-clock"></i> Open Hours: Mon - Sat - 9:00 -
              18:00</span
            >
          </div>
          <div class="infos">
            <div class="phone">
              <span> <i class="fa-solid fa-phone"></i> +1(305) 1234-5678 </span>
            </div>
            <div class="mail">
              <span
                ><i class="fa-solid fa-envelope"></i> hello@example.com</span
              >
            </div>
            <div class="social">
              <span
                ><a href="#"><i class="fa-brands fa-facebook"></i></a
              ></span>
              <span
                ><a href="#"><i class="fa-brands fa-twitter"></i></a
              ></span>
              <span
                ><a href="#"><i class="fa-brands fa-linkedin"></i></a
              ></span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- sezione hero -->
    <div class="hero">
      <AppBackground />
      <div class="container">
        <div class="mainHeader center-align">
          <div><img class="logo" src="../assets/logo.PNG" alt="logo" /></div>
          <!-- navigation -->
          <nav class="center-align">
            <div v-for="link in links">
              <span
                ><a href="">{{ link }}</a></span
              >
            </div>
            <div class="butTouch">
              <button class="btn">GET IN TOUCH</button>
            </div>
          </nav>
        </div>
        <!-- contenuto centrale -->
        <div class="mainTitle">
          <div class="title">
            <h1 class="first">Ready</h1>
            <h1 class="second">Team</h1>
          </div>
          <p class="slogan light-text">
            No matter what your company needs, we will be ready to assist you in
            the best possible way.
          </p>
          <div class="buttons">
            <button class="btn">GET IN TOUCH</button>
            <button class="btn-light">READ MORE</button>
          </div>
        </div>
      </div>
    </div>
    <!-- effetto barra laterale -->
    <div class="v-nav">
      <div></div>
      <div class="full"></div>
      <div></div>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  color: var(--text-color-light);
  overflow-x: hidden;
  overflow-y: hidden;
  .v-nav {
    position: absolute;
    right: 1%;
    top: 50%;
    div {
      margin: 0.625rem 0;
      height: 3.125rem;
      width: 0.625rem;
      border: 0.0625rem solid var(--primary-color);
      border-radius: 1.25rem;
    }
    .full {
      height: 3.125rem;
      width: 0.625rem;
      border: 0.0625rem solid var(--primary-color);
      background-color: var(--primary-color);
      border-radius: 1.25rem;
    }
  }
  .preHeader {
    display: flex;
    justify-content: space-between;
    span {
      margin-left: var(--margin);
      a {
        color: var(--text-color-light);
      }
    }

    .infos {
      display: flex;
      justify-content: space-between;
      .social,
      .mail,
      .phone {
        margin-left: var(--margin);
      }
    }
  }
  .mainHeader {
    color: var(--text-color-dark);
    justify-content: space-between;
    .logo {
      width: 50%;
    }
    nav {
      div {
        margin-left: var(--margin);
        a {
          color: var(--text-color-dark);
        }
      }
      .butTouch {
        margin-left: var(--margin);
      }
    }
  }

  .bgc {
    background-color: #21333e;
    padding: 0.625rem 0rem;
  }

  .hero {
    padding-top: var(--padding-small);
    height: 53.125rem;
    position: relative;
    background-image: url("src/assets/bg-parallax.png");
    background-position: center;
    .mainTitle {
      width: calc(var(--container) / 3);
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      .title {
        display: flex;
        font-weight: 900;
        margin-bottom: var(--margin);
        h1 {
          font-weight: 1200;
          font-size: 5rem;
        }
      }
      .buttons {
        width: 80%;
        margin-top: var(--margin);
        display: flex;
        justify-content: space-between;
        .btn-light:hover {
          background-color: var(--primary-color);
          color: #fff;
          border: 0.0625rem solid #fff;
          padding: 0.625rem 1.25rem;
          border-radius: 0.125rem;
          cursor: pointer;
        }
      }
    }
  }
}
</style>
