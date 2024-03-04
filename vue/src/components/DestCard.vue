
 <template>
  <div>
    <h2 class="header">SHOPPING CART</h2>
    <cart class="ShoppingCart" :cart="this.cart" :total="this.total"> </cart>
  </div>
    <div class="cards">
      <img :src="bedthing.img" alt="bedthing.name"/>
      <h2>{{ bedthing.name }}</h2>
      <h3>${{ bedthing.price }}</h3>
      <button v-on:click=add>add to cart</button> 
  </div>
      
  </template>

  <script setup>
  //import { ref } from "vue";
  const props = defineProps ({
    cart: Array,
    bedthing: Object,
    emits: ['card']
  })
  function add(){
    console.log(bedthing.name);
  }
  </script>

<style scoped>
img{
    width:314px;
    height: 300px;
    object-fit: cover;
}
.cards{
    background-color: rgb(234, 234, 234);
    align-items: center;
    justify-content: center;
    padding: 5px;
    margin: 5px;
    width: 325px;
}
</style>