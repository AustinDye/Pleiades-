<template>
  <div id="whyus" class="container d-block d-lg-flex justify-content-center">
    <div class="wrapper w-30 rounded-left d-flex">
      <div class="row main-row justify-content-center align-items-center">
        <div class="col-12 text-center">
          <div class="d-block">
            <b>We</b>
            <b class="dark-side">Use</b>
          </div>
        </div>

        <div
          class="col-6 col-lg-12 d-flex justify-content-center align-items-center"
          v-scrollanimation
        >
          <img
            loading="lazy"
            class="img-brand"
            src="../assets/img/vue.png"
            alt=""
          />
        </div>
        <div
          class="col-6 col-lg-12 d-flex justify-content-center align-items-center"
          v-scrollanimation
        >
          <img
            loading="lazy"
            class="img-brand"
            src="../assets/img/shopify.png"
            alt=""
          />
        </div>
        <div
          class="col-6 col-lg-12 d-flex justify-content-center align-items-center"
          v-scrollanimation
        >
          <img
            loading="lazy"
            class="img-brand"
            src="../assets/img/wordpress.png"
            alt=""
          />
        </div>
        <div
          class="col-6 col-lg-12 d-flex justify-content-center align-items-center"
          v-scrollanimation
        >
          <img
            loading="lazy"
            class="img-brand azure"
            src="../assets/img/azure.png"
            alt=""
          />
        </div>
      </div>
    </div>

    <div class="wrapper w-70 rounded-right d-flex">
      <div class="row justify-content-between align-items-center">
        <div
          class="col-md-12 d-flex flex-column justify-content-center align-items-center my-2"
          v-scrollanimation
        >
          <div class="d-md-flex">
            <b class="dark-side">Customized </b>
            <b>Experience</b>
          </div>

          <p class="body-text">
            At Pleiades, we specialize in creating custom websites for
            businesses and organizations of all sizes. We take pride in our
            ability to understand our clients' needs and goals, and use that
            understanding to craft visually stunning and highly functional
            websites. Our team of experienced designers and developers work
            closely with each client to ensure that their website is not only
            visually appealing, but also effectively communicates their brand
            and meets the needs of their target audience. Whether you need a
            simple brochure website or a complex e-commerce platform, we have
            the skills and expertise to bring your vision to life.
          </p>
        </div>
        <div
          class="col-md-12 d-flex flex-column justify-content-center align-items-center my-2"
          v-scrollanimation
        >
          <div class="d-md-flex">
            <b>Web </b>
            <b class="dark-side">Apps</b>
          </div>
          <p class="body-text">
            Our web application development services include custom web app
            development, e-commerce applications, content management systems
            (CMS) and business automation. With custom web app development, our
            team will work closely with you to understand your business needs
            and create a custom web application that streamlines your operations
            and improves productivity.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.before-enter {
  opacity: 0;
  transform: translatex(70%);
  transition: all 0.5s ease;
}

.enter {
  opacity: 1;
  transition-delay: 0.3s;
  transform: translatex(0);
}

.container {
  height: 100vh;
  margin-top: 15vh;
}

b {
  font-size: 3em;
  position: relative;
  z-index: 2;
  padding: 0.2em;
  text-align: center;

  @media (max-width: 280px) {
    font-size: 2em;
  }
}
.dark-side {
  background-color: black;
  color: white;

  border-radius: 25px;
  max-width: 100%;
}

p {
  font-size: 1.2em;

  @media (max-width: 280px) {
    font-size: 1em;
  }
}

.wrapper {
  padding: 3em;
  height: 100%;
  background-color: rgb(255, 255, 255);
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: center;
  @media (max-width: 900px) {
    height: 100%;
    width: 100%;
    border-radius: 25px;
  }
}

.wrapper-2 {
  padding: 5em;
  background-color: rgb(255, 255, 255);
  display: flex;
  align-self: center;
  justify-content: center;
  align-items: center;
  @media (max-width: 900px) {
    height: auto;
    border-radius: 25px;
    margin-top: 15vh;
    padding: 2.5em;
  }
}

.rounded-left {
  border-radius: 25px 0px 0px 25px;
}
.rounded-right {
  border-radius: 0px 25px 25px 0px;
}

.wrapper-2 h2 {
  font-size: 3em;

  @media (max-width: 280px) {
    font-size: 1em;
  }
}
.img-brand {
  display: flex;
  justify-content: center;
  align-items: center;
  max-height: 10vh;

  margin-top: 2em;
  @media (max-width: 900px) {
    max-height: 7vh;
  }
}

.azure {
  max-height: 10vh;

  padding: 1em;
  @media (max-width: 900px) {
    max-height: 9vh;
    margin-left: 15%;
  }
}

.body-text {
  padding-top: 2.5vh;
}

.letter-circle {
  background: #ffb625a3;
  z-index: -1;
  width: 6vh;
  height: 6vh;
  border-radius: 100%;
  position: absolute;
  bottom: 0;
  right: -1vw;
}

#circle-2 {
  left: 2em;
  background: #0d5bd88f;
}

#circle-3 {
  right: 2em;
  background: #fd4715a0;
}
</style>