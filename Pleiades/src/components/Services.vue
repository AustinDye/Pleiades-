<template>
    <div id="services" class="row g-0 m-0" v-scrollanimation>
        <div class="col-12"><h1>Experts on the Web</h1></div>
    </div>
    <div class="container about-section" v-scrollanimation>
        <div class="row justify-content-center align-items-center p-5 " >
            <div class="col-12" v-scrollanimation>
                <div class="card-holder">
                     
                    <div class="text-wrapper">
                        <b >Digital  </b>
                        <b class="dark-side">Experiences</b>
                        <p class="body-text">Pleiades Projectworks is a web development company that specializes in creating custom digital experiences for our clients. We understand that every business is unique and that's why our approach is centered around creating custom designs that reflect your brand and message. Our team of expert designers and developers are well-versed in using the latest front-end technologies such as Vue.js, Shopify, and Wordpress to bring your vision to life.</p>
                    </div>
                    <img loading="lazy" class="image-icon d-none d-lg-flex" id="seo" src="../assets/img/custom.png" alt="">
                </div>
            </div>
            <div class="col-12" v-scrollanimation>
                <div class="card-holder">
                    <img  loading="lazy" class="image-icon d-none d-lg-flex" id="seo" src="../assets/img/seo.png" alt="">
                    <div class="text-wrapper">
                        <b>Ecommerce </b>
                        <p class="body-text">Our approach is centered around creating a seamless shopping experience for your customers, from browsing to checkout. We take into consideration factors such as user experience, website speed, and mobile responsiveness to ensure that your customers have a positive experience when shopping on your website. Our team also provides ongoing support and maintenance to ensure that your store is always running smoothly. Trust Pleiades Projectworks to create a custom ecommerce platform that will help you take your business to the next level.</p>
                    </div>
                </div>
            </div>
            <div class="col-12" v-scrollanimation>
                <div class="card-holder">
                    <div class="text-wrapper">
                        <b>Online  </b>
                        <b class="dark-side">Presence</b>
                        <p class="body-text">We work with our clients to create a comprehensive SEO strategy that not only helps increase visibility but also drive targeted traffic to their website. Trust Pleiades Projectworks for all your web development needs and let us help you take your online presence to the next level through our SEO services</p>
                    </div>
                    <img  loading="lazy" class="image-icon d-none d-lg-flex" id="fullstack" src="../assets/img/coding.png" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

h1{
 
    color: white;
    font-size: 10em;
    font-family: geo-medium;
    padding-bottom: 5vh;
    text-align: center;

    @media (max-width: 480px) {
       font-size: 5em;
        
    }

     /* Media Query for Tablets Ipads portrait mode */
     @media (min-width: 768px) and (max-width: 1024px){
      
        font-size: 7em;
    }
  
}

.container{
    
    @media (max-width: 480px) {
        padding: 0;
  
     }
}

@keyframes slideIn {
    0% {
      transform: translateX(50%);
      opacity: 0;
    }
    100% {
      transform: translateX(0);
      opacity: 1;
    }
  }

.body-text{
    padding-top: 2.5vh;
}

.about-section{
    background: white;
    border-radius: 25px;
    width: 95vw;

}

.before-enter {
    opacity: 0;
    transform: translateY(30%);
    transition: all 0.5s ease;
  }
  
  .enter {
    opacity: 1;
    
    transform: translateY(0);
  }
.card-holder{
    padding: 3em;
    border-radius: 25px;
    backdrop-filter: blur(5px);
    display: flex;
    @media (max-width: 480px) {
        padding: 0;
  
     }
     width: 100%;
}

.dark-side{
    background-color: black;
    color: white;
    font-size: .2em;
    padding: .2em;
    border-radius: 25px;

}

.text-wrapper{
  font-family: geo-medium;
  height: 100%;
  padding: 1em;
  @media (max-width: 480px) {
    padding: 0;

 }


}


.text-wrapper b{
    font-size: 3em;
    font-family: geo-medium;
    position: relative;

    @media (max-width: 280px) {
       
        font-size: 2em;
       }

   
}

.text-wrapper p {
    font-size: 1.2em;
    font-family: geo-light;

    @media (max-width: 280px) {
       
        font-size: 1em;
       }
}

img {
    width: 50%;

       @media (max-width: 480px) {
        width: 25%;
        height: 25%;
         
     }

}

#seo{
   padding-top: 5vh;
    height: 50%;
}

</style>