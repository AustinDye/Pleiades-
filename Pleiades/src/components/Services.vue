<template>
    <div class="row g-0 m-0">
        <div class="col-12"><h1>Experts on the Web</h1></div>
    </div>
    <div class="container about-section">
        <div class="row justify-content-center align-items-center p-5">
            <div class="col-12">
                <div class="card-holder">
                     
                    <div class="text-wrapper">
                        <b >Digital  </b>
                        <b class="dark-side">Experiences</b>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi dolor iure saepe obcaecati accusamus, vel assumenda explicabo voluptas recusandae, quidem amet magni laudantium quam laboriosam. Eveniet maiores alias nemo soluta!</p>
                    </div>
                    <img class="image-icon d-none d-lg-flex" id="seo" src="../assets/img/custom-svg.svg" alt="">
                </div>
            </div>
            <div class="col-12">
                <div class="card-holder">
                    <img class="image-icon d-none d-lg-flex" id="seo" src="../assets/img/seo-svg.svg" alt="">
                    <div class="text-wrapper">
                        <b>Ecommerce </b>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi dolor iure saepe obcaecati accusamus, vel assumenda explicabo voluptas recusandae, quidem amet magni laudantium quam laboriosam. Eveniet maiores alias nemo soluta!</p>
                    </div>
                </div>
            </div>
            <div class="col-12">
                <div class="card-holder">
                    <div class="text-wrapper">
                        <b>Online  </b>
                        <b class="dark-side">Presence</b>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi dolor iure saepe obcaecati accusamus, vel assumenda explicabo voluptas recusandae, quidem amet magni laudantium quam laboriosam. Eveniet maiores alias nemo soluta!</p>
                    </div>
                    <img class="image-icon d-none d-lg-flex" id="fullstack" src="../assets/img/coding.svg" alt="">
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
    width: 100%;
    @media (max-width: 480px) {
        padding: 0;
  
     }
}

.about-section{
    background: white;
    border-radius: 25px;
    width: 95vw;
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



#letter-circle-3{

}

.text-wrapper b{
    font-size: 3em;
    font-family: geo-medium;
    position: relative;

   
}

.text-wrapper p {
    font-size: 1.2em;
    font-family: geo-light;
}

img {
    width: 50%;

       @media (max-width: 480px) {
        width: 25%;
        height: 25%;
         
     }

}


</style>