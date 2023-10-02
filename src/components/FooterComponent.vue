<template>
    <footer>
      <div class="footer-content">
        <div class="footer-section">
          <h4>About Us</h4>
          <p>We are a family run Local Australian Business, our passion lies in rich community interactions and building up the local enviroment</p>
        </div>
        <div class="footer-section">
          <h4>Quick Links</h4>
          <ul>
            <li><RouterLink to="/">Home</RouterLink></li>
            <li><RouterLink to="/about">About</RouterLink></li>
            <li><RouterLink to="/products">Products</RouterLink></li>
            <li><RouterLink to="/login">Sign In</RouterLink></li>
            <li><RouterLink to="/checkout/cart">Checkout</RouterLink></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>Contact Info</h4>
          <p style="padding-left: 12px;">123 Street, Deakin University, Burwood, Australia</p>
          <p style="padding-left: 12px;">+1 234 567 890</p>
          <p style="padding-left: 12px;"><a href="mailto:jpyrczak@deakin.edu.au">jpyrczak@deakin.edu.au</a></p>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2023 Jake Pyrczak. All rights reserved.</p>
      </div>
    </footer>
  </template>
  
  <script setup>
  // You can add any reactive properties or methods if needed.
  </script>
  
  <style scoped>
  footer {
    background-color: #334088;
    color: #ecf0f1;
    padding: 20px 0;
    font-family: inherit;
    font-size: 0.9rem;
  }
  
  .footer-content {
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    padding: 0 20px;
  }
  
  .footer-section {
    flex: 1;
    margin-right: 20px;
  }
  
  .footer-section:last-child {
    margin-right: 0;
  }
  
  .footer-section h4 {
    border-bottom: 2px solid rgb(197, 68, 68);
    padding-bottom: 10px;
    margin-bottom: 20px;
  }
  
  .footer-section p, .footer-section li {
    margin-bottom: 7px;
  }
  
  .footer-section a {
    color: #ecf0f1;
    text-decoration: none;
    transition: color 0.5s;
  }
  
  .footer-section a:hover {
    color: #d86b6b;
  }
  
  .footer-bottom {
    text-align: center;
    margin-top: 20px;
    border-top: 1px solid #626262;
    padding-top: 20px;
  }

  </style>
  