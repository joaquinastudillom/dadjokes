<template>
  <div class="container">
    <b-card
      border-variant="primary"
      header="Joke"
      header-bg-variant="primary"
      header-text-variant="white"
      align="center"
    >
      <b-card-text>{{joke}}</b-card-text>
      <b-button variant="primary">
          <nuxt-link to="/jokes">Go back</nuxt-link>
      </b-button>
    </b-card>
  </div>
</template>
    
<script>
import axios from "axios";
export default {
  data() {
    return {
      joke: {}
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data.joke;
    } catch (error) {
      console.log(error);
    }
  }
};
</script>
    
<style scoped>
a{
    color: white;
}
</style>
