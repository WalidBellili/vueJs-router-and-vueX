<template>


  <div class="home">
    <div class="products">
      <div v-for="(product, index) in this.products" :key="index" class="product">
      <div class="product-image" :style="{backgroundImage : 'url(' + product.image + ')'}">
      </div>
      <h4>{{product.title}}</h4>
      <p class="price">US$ {{product.price}}</p>
      <button>Add</button>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'HomeView',
  // data() {
  //   return {
  //     products: this.$store.state.products
  //   }
  // },
  computed: {
    products() {
      return this.$store.state.products
    }
  },
  components: {
   
  }
}
</script>
