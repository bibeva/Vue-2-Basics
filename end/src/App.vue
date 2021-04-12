<template>
  <div id="app">
    <!-- header -->
    <header id="header">
      <div class="container">
        <div class="cart">
          <p><i class="fas fa-shopping-cart"></i> {{ cart.length }}</p>
        </div>
      </div>
    </header>

    <product @addtocart="updatecart" :member="member"></product>
  </div>
</template>

<script>
import Product from './components/Product.vue';

export default {
  name: 'App',
  components: {
    Product
  },
  data() {
    return {
      member: true,
      cart: []
    }
  },
  methods: {
    updatecart(id) {
      this.cart.push(id);
    }
  },
}
</script>