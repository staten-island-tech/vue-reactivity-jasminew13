<template>
    <h2 class="header">SHOPPING CART</h2>
    <cart class="ShoppingCart" :cart="this.cart" :total="this.total"> </cart>
</template>
<script>
export { props } from "DestCard.vue"
import { bedthings } from "./HomeView.vue" 
export default {
    props: ['bedthings', 'cart'],
    data() {
      return {}
    },
    emits: {
      addToCart(e) {
        this.$emit('cart', e)
      }
    },
    emptycart(){
        this.cart= [];
        this.total = 0;
    },
  }

</script>
<style scoped>

.ShoppingCart{
  width: 50rem;
  background-color: brown;
}
.header{
  line-height: 1.5%;
}

</style>