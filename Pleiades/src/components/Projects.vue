<template>


        <div class="container">
            
            <div class="row">
                <div class="col-12 col-md-6">
                    <swiper
                    :effect="'cards'"
                    :grabCursor="true"
                    :modules="modules"
                    class="mySwiper"
                  >
                    <swiper-slide>
                        <div class="row justify-content-center align-items-center">
                           
                            <div class="col-12 img-brand"><img src="/src/assets/img/portsches-logo.webp" alt=""></div>
                            <div class="col-12 d-flex justify-content-center align-items-center flex-column">
                                <ul>
                                    <li>Shopify Storefront</li>
                                    <li>Vue.js Diamond Picker</li>
                                    <li>Vue.js Apointment Calandar</li>
                                    <li>Custom Web Design</li>
                                </ul>
                                <a href="">Check out the site!</a>
                            </div>
                        </div>
                    </swiper-slide>
                    <swiper-slide>
                        <div class="row justify-content-center align-items-center">
                           
                            <div class="col-12 img-brand deb"><img src="/src/assets/img/debdye.png" alt=""></div>
                            <div class="col-12 d-flex justify-content-center align-items-center flex-column">
                                <ul>
                                    <li>Shopify Storefront</li>
                                    <li>Vue.js Diamond Picker</li>
                                    <li>Vue.js Apointment Calandar</li>
                                    <li>Custom Web Design</li>
                                </ul>
                                <a href="">Check out the site!</a>
                            </div>
                        </div>
                    </swiper-slide>
                    <swiper-slide>Slide 3</swiper-slide>
              
                  </swiper>
                </div>
                <div class="col-6"></div>
            </div>
            
            <!--<div class="row justify-content-center align-items-center">
                <div class="col-12"></div>
                <div class="col-12 col-md-4 img-brand deb"><img src="../assets/img/Screenshot 2023-01-01 at 11.13.37 AM.png" alt=""></div>
                <div class="col-12 col-md-4 img-brand"><img src="../assets/img/portsches-logo.webp" alt=""></div>
                <div class="col-12 col-md-4 img-brand"><h5>Show up here! Be our next project.</h5></div>
        
            </div>-->

       
        </div>

</template>

<script>
    // Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/effect-cards";

import "../assets/main.css";

// import required modules
import { EffectCards } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [EffectCards],
    };
  },
};
</script>

<style lang="scss" scoped>
.container{
    margin-top: 7vh;
    padding: 2em;
    padding-right: 10em;
    background: url('/src/assets/img/background.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    border-radius: 25px;
    color: black;
    font-family: geo-light;

    @media (max-width: 480px) {
        background: none;
       }
}

ul{
    padding-top: 1em;
    color: black;
    font-family: geo-light;
    font-size: .8em;
}

a{
    padding: 1em;
    text-decoration: none;
}



.img-brand{
    padding: .5em;
    display: flex;
    justify-content: center;
    align-items: center;

    font-family: geo-medium;

    @media (max-width: 480px) {
        margin-top: 1em;      
    }
}

.img-brand img{
    width: 75%;
}

.deb{
    width: 80%;
    background-color: #5E0149;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 30px;
    padding-bottom: 4em;
    padding-top: 4em;
    @media (max-width: 480px) {
        margin-top: 1em;
        padding-top: 3em;
        padding-bottom: 3em;      
    }
   
}

</style>