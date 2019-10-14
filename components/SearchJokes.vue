<template>
  <div style="padding:20px">
    <b-form inline @submit.prevent="onSubmit">
      <label class="sr-only" for="inline-form-input-name">Name</label>
      <b-input id="inline-form-input-name" class="mb-2 mr-sm-2 mb-sm-0" placeholder="Search Jokes..." v-model="text"></b-input>
      <b-button type="submit" variant="primary">Search</b-button>
    </b-form>
  </div>
</template>
    
<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: ""
    };
  },
  methods: {
      onSubmit(){
          this.$emit('search-text', this.text);
          this.text = "";
      }
  }
};
</script>
    
<style scoped>
</style>
