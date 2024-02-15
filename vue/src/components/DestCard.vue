
 <template>
    <div class="cards">
      <img :src="bedthing.img" alt="bedthing.name"/>
      <h2>{{ bedthing.name }}</h2>
      <h3>${{ bedthing.price }}</h3>
      <button @click="increment" >add {{ clicked }}</button> 
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

  function addcart (){
    increment
    
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
.container{
  display: flex;
  flex-wrap: wrap;
}


</style>