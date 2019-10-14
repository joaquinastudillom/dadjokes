<template>
  <div>
    <b-navbar toggleable="sm" type="light" variant="light">
      <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>

      <b-navbar-brand>DadJokes</b-navbar-brand>

      <b-collapse id="nav-text-collapse" is-nav>
        <b-navbar-nav right>
          <b-nav-item><nuxt-link to="/">Home</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="/jokes">Jokes</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="/about">About</nuxt-link></b-nav-item>
        </b-navbar-nav>
      </b-collapse>

    </b-navbar>
  </div>
</template>
    
<script>
export default {
  name: "AppHeader"
};
</script>
    
<style scoped>
</style>
