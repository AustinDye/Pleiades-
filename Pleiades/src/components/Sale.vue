<template>
    <div class="container d-block d-lg-flex">
      
    <div class="wrapper d-flex">
            <div class="row justify-content-center align-items-center ">
                <div class="col-12 text-center">  
                    <div class="d-block">
                        <b>We</b>
                        <b class="dark-side">Use</b>
                    </div>
                </div>

                <div class="col-6 col-lg-12 d-flex justify-content-center align-items-center "><img class="img-brand" src="https://www.positivethinking.tech/wp-content/uploads/2021/01/Logo-Vuejs.png" alt=""></div>
                <div class="col-6 col-lg-12 d-flex justify-content-center align-items-center "><img class="img-brand" src="https://images.g2crowd.com/uploads/product/image/social_landscape/social_landscape_84fd5bd582809f20ff5682d2746ffa82/shopify.png" alt=""></div>
                <div class="col-6 col-lg-12 d-flex justify-content-center align-items-center "><img class="img-brand" src="https://s.w.org/style/images/about/WordPress-logotype-alternative.png" alt=""></div>
                <div class="col-6 col-lg-12  d-flex justify-content-center align-items-center  "><img class="img-brand azure" src="https://www.dbcloudbin.com/wp-content/uploads/2019/07/azure_logo_794_new.png" alt=""></div>
        
            </div>
        </div>

        <div class="wrapper-2">
            <div class="row flex-column justify-contnet-center align-items-center">
                <div class="about-section d-flex">
                 
                        <div class="row justify-content-center align-items-center">
                            <div class="col-md-12 d-flex flex-column justify-content-center align-items-center">
                                <div class="d-md-flex">
                                    <b class="dark-side">Customized </b>
                                    <b>Experience</b>
                                </div>
                              
                                <p>At Pleiades, we specialize in creating custom websites for businesses and organizations of all sizes. We take pride in our ability to understand our clients' needs and goals, and use that understanding to craft visually stunning and highly functional websites. Our team of experienced designers and developers work closely with each client to ensure that their website is not only visually appealing, but also effectively communicates their brand and meets the needs of their target audience. Whether you need a simple brochure website or a complex e-commerce platform, we have the skills and expertise to bring your vision to life.</p>
                            </div>
                            <div class="col-md-12 d-flex flex-column justify-content-center align-items-center">
                                <div class="d-md-flex">
                                    <b>Customized </b>
                                    <b class="dark-side">Experience </b>
                                </div>
                                <p>At Pleiades, we specialize in creating custom websites for businesses and organizations of all sizes. We take pride in our ability to understand our clients' needs and goals, and use that understanding to craft visually stunning and highly functional websites. Our team of experienced designers and developers work closely with each client to ensure that their website is not only visually appealing, but also effectively communicates their brand and meets the needs of their target audience. Whether you need a simple brochure website or a complex e-commerce platform, we have the skills and expertise to bring your vision to life.</p>
                            </div>
                        </div>
                
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

.container{
    margin-top: 15vh;
}

b{
    font-size: 3em;
    font-family: geo-medium;
    position: relative;
    z-index: 2;
    padding: .2em;
    text-align: center;
}
.dark-side{
    background-color: black;
    color: white;

    border-radius: 25px;
    max-width: 100%;
}

p{
    font-family: geo-light;
    font-size: 1.2em;
}

.wrapper{
  
    width: 35%;
    padding: 10em;
    height: 100vh;
    background-color: rgb(255, 255, 255);
    display: flex;
    justify-content: center;
    align-items: center;
    align-self: center;
    border-radius:25px 0px 0px 25px;
    padding: 2em;
    @media (max-width: 900px) {
     height: 100%;
     width: 100%;
     border-radius: 25px;
         
    }
}

.wrapper-2{
    padding: 5em;
    background-color: rgb(255, 255, 255);
    display: flex;
    align-self: center;
    border-radius:0px 25px 25px 0px;
    height: 100vh;
    @media (max-width: 900px) {
        height: auto;
        border-radius: 25px;
        margin-top: 15vh;
            
       }
}

.wrapper-2 h2 {
    font-size: 3em;
}
.img-brand{
    display: flex;
    justify-content: center;
    align-items: center;
    max-height: 10vh;
    font-family: geo-medium;
    margin-top: 2em;
    @media (max-width: 900px) {
        max-height: 7vh;
         
     }
}

.azure{
    max-height: 10vh;
    
    padding: 1em;
    @media (max-width: 900px) {
        max-height: 9vh;
        margin-left: 15%;
         
     }

}

.letter-circle{
    background: #ffb625a3;
    z-index: -1;
    width: 6vh;
    height: 6vh;
    border-radius: 100%;
    position: absolute;
    bottom: 0;
    right: -1vw;
}

#circle-2{
    left: 2em;
    background: #0d5bd88f;
}

#circle-3{
    right: 2em;
    background: #fd4715a0;
}
</style>