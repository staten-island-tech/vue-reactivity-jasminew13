<template>
  <div class="cardie">
    <DestCard v-for="bedthing in bedthings" 
    :key="bedthing.name"
    :bedthing="bedthing"/>
  </div>
</template>

<script setup>
import DestCard from "@/components/DestCard.vue";
const bedthings =[
        {
          name: "platform bed frame",
          price: 100,
          img: '/imgs/platformbedframe.webp',
        },
        {
          name: "floor bed frame",
          price: 100,
          img: 'https://m.media-amazon.com/images/I/61KSHVmnt1L._AC_UF894,1000_QL80_.jpg',
        },
        {
          name: "soft mattress",
          price: 500,
          img: 'https://marvel-b1-cdn.bc0a.com/f00000000292629/www.mathishome.com/dw/image/v2/AAYQ_PRD/on/demandware.static/-/Sites-mathisbrothers-master/default/dw32bbca1c/images/products/hires/LA/LA-333033_CKM/LA-333033_CKM_01.jpg?sw=800',
        },
        {
          name: "firm mattress",
          price: 500,
          img: 'https://www.originalmattress.com/content/images/thumbs/0001136_orthopedic-extra-firm-mattress-set_1000.jpeg',
        },

      ]
</script>

<style scoped>
.cardie{
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}

</style>