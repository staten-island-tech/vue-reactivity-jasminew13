<template>
    <div class="cards">
      <h2>{{ Destination.name }}</h2>
      <img :src="Destination.img" :alt="Destination.name"/>
      <h3>${{ Destination.price }}</h3>
      <h3>{{ clicked }}</h3>
      <button @click="increment">click</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  const props = defineProps ({
    Destination: Object,
  })
  //clicker logic
  const clicked = ref(0);
  function increment(){
    clicked.value++;
  }
  </script>

<style scoped>
img{
    width:250px;
    height: 300px;
    object-fit: cover;
}
.cards{
    background-color: rgb(251, 245, 236);
    align-items: center;
    justify-content: center;
}


</style>