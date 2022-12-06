<script>
export default {
  name: "AppSection5",
};
</script>

<template>
  <section>
    <div class="container">
      <div class="left">
        <div class="introSection">
          <span>SEND A MESSAGE</span>
        </div>
        <div class="titleSection center-align">
          <h2>Get</h2>
          <h2 class="second">in Touch</h2>
        </div>
        <div class="light-text">
          <p>We will respond to your message as soon as possible.</p>
        </div>
        <form>
          <div class="up">
            <div class="name">
              <input class="rel" type="text" placeholder="Name" />
              <img src="../../assets/image (1).png" alt="form" />
            </div>
            <input type="text" placeholder="Phone" />
          </div>
          <div class="middle">
            <input type="email" placeholder="Email" />
            <div class="info">
              <select name="info" id="info">
                <option value="" selected>More Info</option>
                <option value="faq">FAQ</option>
                <option value="help">Help</option>
              </select>
              <i class="fa-solid fa-chevron-down"></i>
            </div>
          </div>
          <div class="bottom">
            <textarea placeholder="Message" rows="6" cols="50"></textarea>
          </div>
          <button class="btn">SEND</button>
        </form>
      </div>
      <div class="right">
        <h3>Example Inc.</h3>
        <p class="light-text t">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit placeat
          molestiae, illum recusandae eaque optio deserunt soluta debitis
        </p>
        <p class="light-text">
          cupiditate quos minus aliquid a dolorum quaerat nobis ex sint
          reiciendis praesentium.
        </p>
        <div class="infos light-text">
          <div class="phone">
            <span> <i class="fa-solid fa-phone"></i> +1(305) 1234-5678 </span>
          </div>
          <div class="mail">
            <span><i class="fa-solid fa-envelope"></i> hello@example.com</span>
          </div>
          <div class="position">
            <span
              ><i class="fa-solid fa-location-dot"></i> Main Avenue, 987</span
            >
          </div>
        </div>
        <button class="btn-light">VIEW MAP</button>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
section {
  padding: 5rem 0rem;
}
.container {
  display: flex;

  .btn-light:hover {
    background-color: var(--primary-color);
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 2px;
    cursor: pointer;
  }
  .btn:hover {
    color: var(--primary-color);
    background-color: #fff;
    border: 1px solid var(--primary-color);
    padding: 10px 20px;
    border-radius: 2px;
  }

  .titleSection {
    margin-bottom: var(--margin-small);

    h2 {
      font-size: 3.5rem;
    }
  }
  .left {
    width: 70%;
    padding: var(--padding-small);
    form {
      margin-top: var(--margin);
      .up {
        position: relative;
      }
      .name {
        position: relative;
      }
      img {
        position: absolute;
        right: 1.25rem;
        top: calc(50% - 8px);
      }
      .middle {
        position: relative;
        i {
          position: absolute;
          color: gray;
          right: 1.25rem;
          top: calc(50% - 8px);
        }
      }

      .up,
      .middle,
      .bottom {
        display: flex;
        justify-content: space-between;
        margin-bottom: var(--margin-small);
      }
      input,
      select {
        background-color: #ececec;
        border: none;
        padding: 1.25rem 0.625rem;
        margin: 0.625rem 0;
        width: calc(var(--container) * 0.7 / 2 - 30px);
        appearance: none;
      }
      textarea {
        background-color: #ececec;
        border: none;
        padding: 0.625rem;
        margin: 0.625rem 0;
        width: 100%;
        resize: none;
      }
    }
  }
  .right {
    width: 30%;
    padding: var(--padding-small);
    .t {
      margin-bottom: var(--margin-small);
    }
    h3 {
      margin-bottom: var(--margin-small);
    }
  }
}
.infos {
  color: var(--primary-color);
  display: flex;
  flex-direction: column;
  margin-top: var(--margin-small);
  margin-bottom: var(--margin-small);
  .fa-solid {
    background-color: var(--text-bg-title-lightgreen);
    border-radius: 100%;
    padding: 0.625rem;
    margin: 0.625rem 0;
  }
}
select {
  color: gray;
}
</style>
