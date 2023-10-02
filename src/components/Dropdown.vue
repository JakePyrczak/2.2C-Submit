<template>
  <div class="dropdown">
    <button @click="toggle" class="dropbutton">Menu</button>
    <div v-show="showMenu" class="dropdown-contents">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/products">Products</RouterLink>
      <RouterLink to="/login">Sign In</RouterLink>
      <RouterLink to="/checkout/cart">Checkout</RouterLink>
    </div>
  </div>
</template>

<script setup>

import { ref } from 'vue';
const showMenu = ref(false)

const toggle = () => {
  showMenu.value = !showMenu.value;
};

</script>

<style scoped>
.dropbutton{
  color: #ffffff;
  background: #3f51b5;
  padding: 10px 35px;
  border-radius: 6px;
  transition: background-color 0.4s;
  text-decoration: none;
  font-family: inherit;
  font-size: 1.1rem;
  border-style: none;
  cursor: pointer;
}

.dropbutton:hover{
  background-color: #db2929;
}

 .dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-contents {
  text-align: center;
  position: absolute;
  background-color: #e5e8f1;
  min-width: 250px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
  right: 0;
}

.dropdown-contents a {
  color: black;
  padding: 18px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-contents a:hover {background-color: #909bdd;}

</style>

