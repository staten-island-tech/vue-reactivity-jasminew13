<template>

    <h2 class="header">SHOPPING CART</h2>
    <cart class="ShoppingCart" :cart="this.cart" :total="this.total"> </cart>
</template>
<script>
export { props } from "DestCard.vue"
import { bedthings } from "./HomeView.vue" 
export default {
    name: 'DestCard',
    props: ['bedthing'],
    data() {
      return {}
    },
    methods: {
      addToCart(bedthing) {
        this.$emit('adding', bedthing)
      }
    },
    emptycart(){
        this.cart= [];
        this.total = 0;
    }
  }
</script>
<style scoped>

.ShoppingCart{
    width: 40px;
}
</style>