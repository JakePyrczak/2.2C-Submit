<template>
  <main>
    <div class="main-wrap">
      <div class="background-image"></div>
      <div class="top">
        <h1>Authentic Local Quality at Great Prices</h1>
        <b>
          <p style="margin-bottom: 20px; color: rgb(0, 0, 0)">
            Come check out our wide collection of products, we selling anything
            from clothes, toys, food, and just about anything you could need!
          </p>
        </b>
        <br />
        <RouterLink class="shop-btn" to="/products">Shop Now</RouterLink>
      </div>
    </div>
    <div class="values-section">
      <hr />
      <h2>
        Our Values
      </h2>
      <p>How we are making the community a better place</p>
      <div class="values-boxes">
        <div class="value-box">
    <b>Local Impact</b>
    <p>Our business is committed to making a positive impact on our local community. 
      We source our products locally, support local artisans, and give back to local charities.</p>
  </div>
  <div class="value-box">
    <b>High Quality</b>
    <p>We take pride in delivering products of the highest quality. 
      Our team carefully selects each item to ensure that our 
      customers receive the best possible value.</p>
  </div>
  <div class="value-box">
    <b>Exceptional Service</b>
    <p>Our goal is to provide exceptional customer service. 
      We're here to assist you with any questions or concerns, 
      ensuring your shopping experience is smooth and enjoyable.</p>
  </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
.shop-btn {
  color: #ffffff;
  background: #3f51b5;
  padding: 10px 20px;
  border-radius: 6px;
  transition: background-color 0.4s;
  text-decoration: none;
}

.shop-btn:hover {
  background-color: #db2929;
}

.main-wrap {
  display: block;
  margin-top: 120px;
  position: relative;
  margin-bottom: 150px;
}

.top {
  max-width: 500px;
}

.top h1 {
  font-size: 35px;
  margin-bottom: 25px;
  color: #32429d;
}

.background-image {
  background-image: url("/shops.jpg");
  background-size: cover;
  width: 116.2%;
  height: 200%;
  position: absolute;
  top: -120px;
  left: -8.1%;
  right: 0;
  bottom: 0;
  z-index: -1;
  opacity: 0.6;
}

.values-section h2{
  display: flex;
  margin: 10px 0;
  justify-content: center;
  color: #32429d;
}

.values-section p{
  display: flex;
  justify-content: center;
  color: black;
}

hr {
  border: none;
  border-top: 1px solid #959595;
  /* Set the color and thickness of the line */
  margin: 40px 0;
  /* Adjust the margin to control the spacing around the line */
}

.values-boxes {
  display: flex;
  justify-content: space-between;
  margin-top: 40px;
}

.value-box {
  flex: 1;
  padding: 20px;
  /* background-color: #f1f1f1; */
  border: 1px solid #ccc;
  border-radius: 6px;
  text-align: left;
  margin: 10px;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
}

@media (max-width: 882px) {
  .background-image {
    width: 111%;
    left: -5.5%;
  }

  .values-boxes {
    flex-direction: column; /* Change layout to vertical */
    align-items: center;
  }

  .value-box {
    margin: 10px 0;
  }

}

@media (max-width: 700px) {
  .background-image {
    height: 180%;
  }

  .main-wrap {
    margin-top: 130px;
    margin-bottom: 110px;
  }


}
</style>

<script setup>
import { RouterLink } from "vue-router";
</script>
