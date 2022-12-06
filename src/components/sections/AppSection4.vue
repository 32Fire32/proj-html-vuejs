<script>
export default {
  name: "AppSection4",
  data() {
    return {
      numbers: [
        {
          num: 128,
          descr: "Certifications",
        },
        {
          num: 230,
          descr: "Employees",
        },
        {
          num: 517,
          descr: "Customers",
        },
        {
          num: 94,
          descr: "Country Served",
        },
      ],
      idsrcs: ["4", "5", "1", "2", "3", "4"],
    };
  },
};
</script>

<template>
  <section>
    <div class="container">
      <div class="top">
        <span class="introSection">WHAT ARE WE DOING</span>
        <div class="titleSection center-align">
          <h2 class="firstAbout">Results</h2>
          <h2>in Numbers</h2>
        </div>
        <div class="numbers">
          <div v-for="number in numbers">
            <h3>{{ number.num }}</h3>
            <p>{{ number.descr }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="black">
      <div class="container">
        <div class="partners center-align">
          <div v-for="idsrc in idsrcs">
            <img :src="`src/assets/logo-${idsrc}.png`" :alt="idsrc" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
section {
  background-image: url(../../assets/bg-7.jpg);
  background-position: bottom;
  .top {
    padding-top: 80px;
    display: flex;
    flex-direction: column;
    align-items: center;
    .introSection {
      margin-bottom: 20px;
    }
    .titleSection {
      margin-bottom: 20px;
      h2 {
        font-size: 4rem;
      }
      h2:last-child {
        color: #fff;
      }
    }
  }
  .firstAbout {
    color: #fff;
    background-color: var(--text-bg-title-green);
    padding: 5px 20px;
    margin-right: 5px;
  }
  .numbers {
    padding: 40px;
    display: flex;
    width: 100%;
    justify-content: space-between;
    margin-bottom: 80px;
    div {
      text-align: center;
      padding: 20px;
    }
    h3 {
      color: var(--primary-color);
      font-size: 3rem;
    }
    p {
      color: #fff;
      font-size: 2rem;
    }
  }
  .black {
    background-color: #111117;
    .partners {
      padding: 120px 40px;
      justify-content: space-between;
      filter: brightness(400%);
      img {
        width: 50%;
      }
    }
  }
}
</style>
