<script setup>
import { ref } from 'vue'
import ProductDisplay from '@/components/ProductDisplay.vue'

const cart = ref([])
const premium = ref(true)

const updateCart = (id) => {
  cart.value.push(id)
}
</script>
  
<template>
  <!--navbar-->
  <div class="nav-bar">
    <h2>Learn Vue Mastery</h2>
  </div>
  <!--cart-->
  <div class="cart">Cart({{ cart.length }})</div>
  <ProductDisplay :premium="premium" @add-to-cart="updateCart" @remove-from-cart="removeFromCart"></ProductDisplay>
</template>



//import { ref, computed } from 'vue'
import ReviewForm from '@/components/ReviewForm.vue'
import ReviewList from '@/components/ReviewList.vue'
import socksGreenImage from '@/assets/images/socks_green.jpeg'
import socksBlueImage from '@/assets/images/socks_blue.jpeg'
import removeFromCart from './components/removeFormCart.vue'