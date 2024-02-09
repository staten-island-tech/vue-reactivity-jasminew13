<template>
  <div class="cardie">
    <DestCard v-for="destination in destinations" 
    :key="destination.name"
    :Destination="destination"/>
  </div>
</template>

<script setup>
import DestCard from "@/components/DestCard.vue";
const ingredients =[
        {
          name: "",
          price: 0,


        },

      ]
</script>

<style scoped>
.cardie{
  height: 40vh;
}

</style>