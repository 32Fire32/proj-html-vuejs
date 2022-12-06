<script>
export default {
  name: "AppSection5",
};
</script>

<template>
  <section>
    <div class="container">
      <div class="left">
        <span class="introSection">SEND A MESSAGE</span>
        <div class="titleSection center-align">
          <h2 class="firstAbout">Get</h2>
          <h2 class="second">in Touch</h2>
        </div>
        <div class="light-text">
          <p>We will respond to your message as soon as possible.</p>
        </div>
        <form>
          <div class="up">
            <input type="text" placeholder="Name" />
            <input type="text" placeholder="Phone" />
          </div>
          <div class="middle">
            <input type="email" placeholder="Email" />
            <select name="info" id="info">
              <option value="" selected>More Info</option>
              <option value="faq">FAQ</option>
              <option value="help">Help</option>
            </select>
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
  padding: 80px 0px;
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
    margin-bottom: 20px;

    h2 {
      font-size: 4rem;
    }
  }
  .left {
    width: 70%;
    padding: 20px;
    form {
      margin-top: var(--margin-top);
      .up,
      .middle,
      .bottom {
        display: flex;
        margin-bottom: 20px;
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
}
.infos {
  color: var(--primary-color);
  display: flex;
  flex-direction: column;
  margin-top: 20px;
  margin-bottom: 20px;
  .fa-solid {
    background-color: var(--text-bg-title-lightgreen);
    border-radius: 100%;
    padding: 10px;
    margin: 10px 0;
  }
}
select {
  color: gray;
}
input,
select {
  background-color: #ececec;
  border: none;
  padding: 20px 10px;
  margin: 10px;
  width: 50%;
}
textarea {
  background-color: #ececec;
  border: none;
  padding: 10px;
  margin: 10px;
  width: 100%;
}
</style>
