<template>
  <div class="cardie">
    <DestCard v-for="bedthing in bedthings" 
    :key="bedthing.name"
    :bedthing="bedthings"/>
  </div>
</template>

<script setup>
import DestCard from "@/components/DestCard.vue";
const bedthings =[
        {
          name: "platform bed frame",
          price: 100,
          img: '../assets/platformbedframe.webp',


        },

      ]
</script>

<style scoped>
.cardie{
  height: 40vh;
}

</style>