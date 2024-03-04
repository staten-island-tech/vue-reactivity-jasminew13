
<template>
  <div class="cards">
    <img :src="bedthing.img" alt="bedthing.name"/>
    <h2>{{ bedthing.name }}</h2>
    <h3>${{ bedthing.price }}</h3>
    <button v-on:click=add>add to cart</button> 
</div>
    
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';
const props = defineProps ({
  cart: Array,
  bedthing: Object,
})
const myemits = defineEmits(['add'])
function add(){
  myemits('add', props.bedthing);
}
</script>

<style scoped>
img{
  width:314px;
  height: 300px;
  object-fit: cover;
}
.cards{
  background-color:#E0E2DB;
  align-items: center;
  justify-content: center;
  padding: 5px;
  margin: 5px;
  width: 325px;
}
</style>