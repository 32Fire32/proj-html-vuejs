<script>
export default {
  name: "AppHeader",
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
      <!-- perheader -->
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

    <div class="hero">
      <div class="container">
        <!-- main header -->
        <div class="mainHeader center-align">
          <div><img class="logo" src="../assets/logo.PNG" alt="" /></div>
          <nav class="center-align">
            <div v-for="link in links">
              <span>{{ link }}</span>
            </div>
            <div class="butTouch">
              <button class="btn">GET IN TOUCH</button>
            </div>
          </nav>
        </div>
        <div class="mainTitle">
          <div class="title">
            <h1>Ready</h1>
            <h1>Team</h1>
          </div>
          <p class="slogan">
            No matter what your company needs, we will be ready to assist you in
            the best possible way.
          </p>
          <div class="buttons">
            <button class="btn">GET IN TOUCH</button>
            <button class="btn-light">GET IN TOUCH</button>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  color: var(--text-color-light);
  .preHeader {
    display: flex;
    justify-content: space-between;
    .infos {
      display: flex;
      justify-content: space-between;
      .social,
      .mail,
      .phone {
        margin-left: var(--margin-left);
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
        margin-left: 20px;
      }
      .butTouch {
        margin-left: var(--margin-left);
      }
    }
  }

  span {
    margin-left: var(--margin-left);
    a {
      color: var(--text-color-light);
    }
  }

  .bgc {
    background-color: #21333e;
    padding: 10px 0px;
  }

  .hero {
    padding-top: 20px;
    height: 850px;
    position: relative;
    background-image: url(../assets/bg-parallax.png);
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
        margin-bottom: var(--margin-bottom);
        h1 {
          font-size: 5rem;
        }
        h1:first-child {
          color: var(--text-color-dark);
        }
        h1:last-child {
          background-color: #d5e7e8;
          color: var(--primary-color);
          border-radius: 2px;
        }
      }
      .buttons {
        width: 80%;
        margin-top: var(--margin-top);
        display: flex;
        justify-content: space-between;
      }
    }
  }
}
</style>
