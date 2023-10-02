<template>
  <main>
    <h1 style="margin: 50px 0;">Shop Our Fine Wares</h1>
    <!-- <hr class="title-divider" /> -->
    <!-- Display a list of products -->
    <div class="products-container">
    <div v-for="product in productsList" :key="product.id" class="product">
      <img v-if="product.image" :src="product.image" alt="Product Image" class="product-image" />
      <h2>{{ product.name }}</h2>
      <p>Price: ${{ product.price }}</p>
      <p>Description: {{ product.description }}</p>
    </div>
  </div>
  </main>
</template>

<script setup>
// Define the product data using reactive ref
import { ref } from 'vue';
import { products } from '/src/data/product_data.json';

const productsList = ref(products);

</script>

<style scoped>
/* Add styles for product display */
.products-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 40px;
}

.product {
  width: 48%;  /* Display 2 products per row */
  margin-bottom: 40px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 6px;
  background-color: #f9f9f9;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
  text-align: center;
}

.product-image {
  max-width: 100%;
  max-height: 400px;
  margin-bottom: 10px;
  border-radius: 6px;
}

.title-divider {
  border: none;
  border-top: 1px solid #ccc;
  width: 100%;
  margin-right: auto;
  margin-left: 0;
}


/* Responsive layout */
@media (max-width: 900px) {
  .product {
    width: 100%; /* Display 1 product per row */
  }
}
</style>
