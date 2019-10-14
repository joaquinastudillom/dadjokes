<template>
  <nuxt-link :to="'jokes/'+id">
    <div class="col-md-12" id="joke">
      <b-card bg-variant="light" text-variant="white" class="text-center">
        <b-card-text>
          <span id="joke-text">{{ joke }}</span>
        </b-card-text>
      </b-card>
    </div>
  </nuxt-link>
</template>
    
<script>
export default {
  name: "Joke",
  props: ["id", "joke"]
};
</script>
    
<style scoped>
#joke {
  padding-top: 10px;
  margin: 0 auto;
  font-weight: 400;
}
#joke-text {
  color: gray;
}
</style>
