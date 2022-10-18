<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/>
</template>

<script>
  import axios from 'axios'
  export default {

    created() {
      axios
      .get(`https://fakestoreapi.com/products`)
      .then((response) => {
        console.log(response.data);
      })
    }

  }

</script>

<style lang="scss">

</style>
