<template>
    <div class="cards">
      <img :src="bedthing.img" alt=""/>
      <h2>{{ bedthing.name }}</h2>
      <h3>${{ bedthing.price }}</h3>
      <h3>add to cart: {{ clicked }}</h3>
      <button @click="increment">add</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  const props = defineProps ({
    bedthing: Object,
  })
  //clicker logic
  const clicked = ref(0);
  function increment(){
    clicked.value++;
  }
  </script>

<style scoped>
img{
    width:300px;
    height: 300px;
    object-fit: cover;
}
.cards{
    background-color: rgb(251, 245, 236);
    align-items: center;
    justify-content: center;
    padding: 5px;
    margin: 5px;
    width: 325px;
}


</style>