<template>
  <form
    class="formContainer"
    :action="endpoint"
    @submit="handleSubmit"
    method="POST"
    target="_blank"
  >
    <div class="form-elems">
      <div class="d-flex justify-content-between">
        <div class="d-flex flex-column w-48">
          <label for="name" class="visibility-hidden"></label>
          <input type="text" placeholder="Your name" name="name" required />
        </div>
        <div class="d-flex flex-column w-48">
          <label for="email" class="visibility-hidden"></label>
          <input type="email" placeholder="Email" name="email" required />
        </div>
      </div>
      <label for="message" class="visibility-hidden"></label>
      <textarea
        class="message"
        placeholder="Your message"
        name="message"
        required
      />
    </div>
    <rainbow-button :displayMessage="'Send Us a Message'" />
  </form>
  <div v-if="submitted">
    <h2>Thanks you!</h2>
    <div>We'll be in touch soon.</div>
  </div>
</template>


<script>
import { ref } from "vue";
import RainbowButton from "./RainbowButton.vue";
export default {
  components: { RainbowButton },
  setup() {
    const submitted = ref(false);
    const endpoint =
      "https://public.herotofu.com/v1/35805ee0-912b-11ed-a003-6f0b76086b1c";

    function handleSubmit(formData) {
      setTimeout(() => {
        submitted.value = true;
      }, 100);
    }
    return {
      submitted,
      endpoint,
      handleSubmit,
    };
  },
};
</script>


<style lang="scss" scoped>
.formContainer {
  width: 100%;
}

.form-elems {
  height: 100%;
}

input {
  padding: 0.5em;
  box-shadow: 0px 0px 0px 4px rgb(198, 198, 198);
  border-radius: 5px;
  border: none;
}

.w-48 {
  width: 48%;
}

textarea {
  width: 100%;
  outline: none;
  border-radius: 5px;
  padding: 1rem;
  box-shadow: 0px 0px 0px 4px rgb(198, 198, 198);
  border: none;
  height: 40vh;
  min-height: calc(50px);
  max-height: 50vh;
  margin-top: 1em;
  margin-bottom: 1em;

  @media (max-width: 480px) {
    width: 100%;
  }
}
</style>