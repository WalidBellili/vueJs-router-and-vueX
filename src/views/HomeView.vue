<template>


  <div class="home">
    <div class="products">
      <div v-for="(product, index) in this.products" :key="index" class="product">
      <div class="product-image" :style="{backgroundImage : 'url(' + product.image + ')'}">
      </div>
      <h4>{{product.title}}</h4>
      <p class="price">US$ {{product.price.toFixed(2)}}</p>
      <button @click="addToBag(product)">Add</button>
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
    },
    productsInBag() {
      return this.$store.state.productsInBag
    }
  },
  methods: {
    addToBag(product) {
      product.quantity = 1
      console.log(product);
      this.$store.dispatch("addToBag", product)
    }
  },
  components: {
   
  }
}
</script>
