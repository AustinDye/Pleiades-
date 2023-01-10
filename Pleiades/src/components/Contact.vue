<template>
    <div class="row">
        <div class="col-12"><h1>contact us today</h1></div>
    </div>
    <div class="container justify-content-center align-items-center d-flex">
    <header>
      <form
      class=""
        :action="FORM_ENDPOINT"
        @submit="handleSubmit"
        method="POST"
        target="_blank"
      >
        <div class="">
          <input type="text" placeholder="Your name" name="name" required />
          <input type="email" placeholder="Email" name="email" required />
        </div>

        <div class="d-flex flex-column justify-content-center align-items-center">
          <textarea placeholder="Your message" name="message" required />
          
            <button type="submit">Send us a message</button>
         
        </div>
       
       
      </form>
  
      <div v-if="submitted">
        <h2>Thanks you!</h2>
        <div>We'll be in touch soon.</div>
      </div>
    </header>
</div>
  </template>
  
  <script>
  export default {
    name: "App",
    data: () => ({
      submitted: false,
      FORM_ENDPOINT: "https://public.herotofu.com/v1/35805ee0-912b-11ed-a003-6f0b76086b1c",
    }),
  
    methods: {
      handleSubmit() {
        setTimeout(() => {
          this.submitted = true;
        }, 100);
      },
    },
  };
  </script>

  <style scoped lang="scss">
    .container{
        
        background-color: white;
        width: 50vw;
        height: 65vh;
        border-radius: 25px;
        margin-bottom: 7vh;

        @media (max-width: 480px) {
            width: 90%;
          
             
         }
    }

    h1{
        margin-top: 7vh;
        color: white;
        font-size: 8em;
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

    input{
        padding: .5em;
        margin-left: 1em;
    }

    button{
        background-color: rgba(128, 128, 128, 0.529);
        border-radius: 10px;
        box-shadow: none;
        border: none;
        outline: none;
        width: 90%;
        padding: .5em;
    }

    textarea{
        height: 40vh;
        width: 30vw;
        margin: 1em;

        @media (max-width: 480px) {
            width: 90%;
          
             
         }
    }
  </style>