<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/>
</template>

<script>
  
  export default {

    created() {
      this.$store.dispatch("loadProducts")

      
    }

  }

</script>

<style lang="scss">

</style>
