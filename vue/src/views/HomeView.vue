<template>
  <div class="cardie">
    <DestCard v-for="bedthing in bedthings" 
    :key="bedthing.name"
    :bedthing="bedthing"
    @add="add"/>
  </div>
  <div class="cartname"><h2>your shopping cart</h2>
 <div class="cart" v-for="bedthing in cart" 
    :key="bedthing.name">
    <p class="cartthing">{{ bedthing.name }}</p>
    <p class="cartthing">${{ bedthing.price }}</p>
    
    </div><p>your total is:  ${{ total }}</p></div>
</template>

<script setup>
import {ref} from 'vue';
import DestCard from "@/components/DestCard.vue";
const bedthings =[
        {
          name: "Ilford Sprite 35-II Analog Film Camera",
          price: 35,
          img: 'https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcRnlftpx0xPRSty_PlHjRVv7T-KHQE61LdPRHzcMICfN9hb0Itd603cpDx3NVUNjYUUs97ZHs2bk_HJyNHL5BICe4AG_7VLXvO2gMVfkcDFlEruJ70x12810A&usqp=CAE',
        },
        {
          name: "Fujifilm Instax Mini 12 Instant Film Camera",
          price: 80,
          img: 'https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcRb3NTdUhKmFzWlUMo6xImZSYk0MVaftbyn_E21z_kck3XN3sRHe-iG7Ya-kApCUVYhNvida0doMANVz1R2Jqw8hq87f0Nymxax4bA5bqF9PwFEAe_121fsjZc&usqp=CAE',
        },
        {
          name: "Canon PowerShot ELPH 360 HS",
          price: 100,
          img: 'https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcRlUYkDrAey-qbSOyQUQRKTakCMDdroyBL86eVWvHzpEZhLZq-3-PjKik1Q9LRKfnn51C1JnZl6HaCloACn8C1lXiwgfh-qhLXp8ymO4FTYU1mhpuOeXvkQMw&usqp=CAE',
        },
        {
          name: "Sony Dsc-w830 Digital Camera",
          price: 159.99,
          img: 'https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcSPaMvYjDb2fWzfAApHd8QGoggoBkla6wEbuSmg1hd__-1alylSA_cug5TQkUTeiNdNC56Et8nDQ_OR-GlTE4px6YT0i_YpHqEzukVewX4&usqp=CAE',
        },
        {
          name: "Nikon D50 Digital Camera",
          price: 90,
          img: 'https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcT1qhuZtDfmBzfm193evCf2o39zP_mdiKw_QGY1jjEPpqeBef3DBfPr2YbOsuhpDmXQz3opUzGuFYmXCQkyo18uBLwcNoTqSnI5SgJ97T1DOq9BrflJ8xRcFA&usqp=CAE',
        },
        {
          name: "Kodak Pixpro AZ528 Digital Camera",
          price: 229,
          img: 'https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcQEk3BLKHCeNbV3GtmX06aYbHcOXbtA4eJ3HZ3vTo_coYoYjxsPvWrClX-24pBIEQzQIRxAapLVEqdonT_MMBjquk7s0IS5d3oWUh9wUtkbgxKPYIbIz7dW&usqp=CAE',
        },
        {
          name: "Canon Eos Rebel T7 Digital SLR Camera",
          price: 479,
          img: 'https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcQtqQlozoPME2dLAnz6zEc4CSfUQaFWuVxXQaa6HsaM6cHB--YxsaPmeoYs23YanMj5TxkS0T3GumTz9Dz4Lq3kbgmZEjc6ZBxIpwO2TB4d1wDvwhGu75EOAw&usqp=CAE',
        },
        {
          name: "Andoer V12",
          price: 58,
          img: 'https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcTkCfFkCPMnXnD9AQtCQ38UTRKJHm68SZhAkRhOGYUZMk4VMcFEQYHFoYLCeiCiDAUtS63TBhtbYt0x7kHVjypPpnT3DpXD3SBOxGQhGF4XFm9oLQjBwdgO6A&usqp=CAE',
        },
        {
          name: "Minolta Mn100hdz-bk",
          price: 139,
          img: 'https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcQDDms8iD8rAWapdoUrz-7A3wwnU9XcgR33XPtvelZ16kNq8BXUl68cqguT0vb1eaDLIDnNqrzM0Kd22eGzWw0jeYP41bmHuV0zhfW03ePfYG5Mpk6Tu7laFSk&usqp=CAE',
        },

      ]
      import { defineProps} from 'vue';
      const cart = ref([]);
      const total = ref(0);

  const props = defineProps ({
    cart: Array,
    bedthing: Object,
  })
  function add(e){
    cart.value.push(e);
    console.log(e.name, '$',e.price);
    var carttotal = total.value += e.price
    console.log(carttotal)
  }
</script>

<style scoped>
.cardie{
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  width: 1020px;
}
.cart{
  display: flex;
  flex-direction: column;
  margin-left: 30px;
}
.cartthing{
  background-color: #889696;
  width: 200px;
    align-self: center;
}
.cartname{
  background-color:#D2D4C8;
  text-align: center;
}
.button{
  size: 20px
}

</style>