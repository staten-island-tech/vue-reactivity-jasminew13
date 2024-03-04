<!-- <template>
    <h2 class="header">SHOPPING CART</h2>
    <cart class="ShoppingCart" :cart="this.cart" :total="this.total"> 
    
    </cart>
</template> -->
<script>
import { defineProps } from 'vue';
const props = defineProps({
 cart: Array,
 bedthing: Object
})

</script>
<style scoped>

.ShoppingCart{
  width: 50rem;
  background-color: brown;
  margin-left: 50%;
}
.header{
  line-height: 1.5%;
}

</style>