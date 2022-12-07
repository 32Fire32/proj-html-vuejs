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
          <!-- cycle numbers -->
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
          <!-- cycle partners -->
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
    padding-top: 5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    .introSection {
      margin-bottom: var(--margin-small);
    }
    .titleSection {
      margin-bottom: var(--margin-small);
      h2 {
        font-size: 3.5rem;
      }
      h2:last-child {
        color: #fff;
      }
    }
  }
  .firstAbout {
    color: #fff;
    background-color: rgba($color: #0e272d, $alpha: 0.6);
    padding: 0.3125rem 1.25rem;
    margin-right: 0.3125rem;
  }
  .numbers {
    padding: var(--padding);
    display: flex;
    width: 100%;
    justify-content: space-between;
    margin-bottom: var(--margin-big);
    div {
      text-align: center;
      padding: var(--padding-small);
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
      padding: 7.5rem 2.5rem;
      justify-content: space-between;
      filter: brightness(400%);
      img {
        width: 50%;
      }
    }
  }
}
</style>
