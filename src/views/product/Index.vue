<template>
  <div>
      <div id="page-wrap">
          <div class="grid-wrap">
            <ProductItem 
              v-for="product in products"
              :key="product.id"

              :product="product"
            />
          </div>
            <!-- <ProductItem 
              v-for="(product, index) in products"
              :key="index"

              :product="product"
            />
          </div> -->
      </div>
  </div>
</template>

<script>
import { products } from '../../data-seed';

//import axios from 'axios';

import ProductItem from '../../components/ProductItem'

export default {
  name: 'ProductIndex', // Ubah dari 'Index'
  
  components: {
    ProductItem
  },
  data() {
      return {
        products
          //products: []
      }
  },
  /* async created() {
  try {
    const result = await axios.get('http://localhost:8000/api/products');
    this.product = result.data;
  } catch (error) {
    console.error("Error fetching products:", error);
  } 
} */

}
</script>

<style scoped>
  .grid-wrap {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-top: 16px;
  }
</style>