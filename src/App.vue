<script setup>
import { RouterLink, RouterView } from "vue-router";
import FooterComp from "./components/FooterComponent.vue";
import Dropdown from "./components/Dropdown.vue";
</script>

<template>
  <header>
    <div class="h-wrapper">
      <div class="logo-align">
        <RouterLink to="/">
          <img alt="Your Logo" class="logo" src="/logo.PNG" />
        </RouterLink>
      </div>

      <div class="mobile-button">
        <Dropdown />
      </div>

      <div class="nav-style">
        <div class="main-nav">
          <RouterLink class="nav-link" to="/">Home</RouterLink> |
          <RouterLink class="nav-link" to="/about">About</RouterLink> |
          <RouterLink class="nav-link" to="/products">Products</RouterLink>
        </div>
        <div class="right-side">
          <RouterLink class="nav-link" to="/login">Sign In</RouterLink>
          <RouterLink class="navbox" to="/checkout/cart">Checkout</RouterLink>
        </div>
      </div>
    </div>
  </header>

  <div class="page-container">
    <div class="content-wrapper">
      <RouterView />
    </div>

    <footer>
      <FooterComp />
    </footer>
  </div>
</template>

<style scoped>
.h-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  max-width: 1100px;
  max-height: 100vh;
  border-bottom: 1px solid #acacac;
  background-color: white;
  position: fixed;
  z-index: 1;
}

.logo {
  margin-right: 4rem;
  padding: 12px 0;
}

.logo-align {
  display: flex;
  justify-content: flex-start;
}

.main-nav {
  display: flex;
  justify-content: center;
}

.nav-link {
  text-decoration: none;
  color: #3498db;
  transition: 0.4s;
  padding: 0 20px;
  margin: 0 10px;
}

.nav-link:hover {
  color: #db2929;
}

.nav-link.router-link-active {
  color: #202f83;
  position: relative;
}

.nav-link.router-link-active::before {
  content: "";
  /*Create an empty pseudo-element */
  position: absolute;
  /* Set absolute positioning */
  bottom: -25px;
  /* Adjust this value to align with the header line */
  left: 0;
  /* Align the pseudo-element with the link text */
  width: 100%;
  /* Make the pseudo-element span the full width */
  border-bottom: 2px solid #202f83;
  /* Add the underline styling */
}

.nav-style {
  font-size: 1.05rem;
  padding: 13px 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.right-side {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  margin: 0 2rem;
}

.navbox {
  color: #ffffff;
  background: #3f51b5;
  padding: 10px 20px;
  border-radius: 6px;
  transition: background-color 0.4s;
  text-decoration: none;
}

.navbox:hover {
  background-color: #db2929;
}

.navbox.router-link-active {
  background-color: #208352;
}

.page-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  /* This ensures the container takes at least most of the viewport */
}

.content-wrapper {
  flex: 1;
  /* This makes the content take up all available space, pushing the footer to the bottom */
  margin: 70px 7%;
}

footer {
  margin-top: 30px;
}

.mobile-button {
  display: none;
}

/* Media query for small screens */
@media (max-width: 882px) {
  .mobile-button {
    display: flex;
    padding: 0 25px;
  }

  .nav-style {
    display: none;
  }

  .content-wrapper {
    margin: 70px 5%;
  }

  footer {
  margin-top: 20px;
}
}
</style>
