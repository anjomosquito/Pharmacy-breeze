
<!--
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->
<template>
    <AuthenticatedLayout>
    <div class="donation-form">
      <h1>Donation Form</h1>
      <form @submit.prevent="submit">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="name" required>
        </div>
        <div class="form-group">
          <label for="price">Price</label>
          <input type="text" id="price" v-model="price" required>
        </div>
        <div class="form-group">
          <label for="middleName">Middle Name:</label>
          <input type="text" id="middleName" v-model="middleName">
        </div>
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="date">Date:</label>
          <input type="date" id="date" v-model="date" required>
        </div>
        <div class="form-group">
          <label for="amount">Donation Amount:</label>
          <input type="number" id="amount" v-model.number="amount" required min="1">
        </div>
        <div class="form-group">
          <label for="paymentMethod">Payment Method:</label>
          <select id="paymentMethod" v-model="paymentMethod" required>
            <option value="gcash">GCash</option>
            <option value="paypal">PayPal</option>
            <option value="paymaya">PayMaya</option>
          </select>
        </div>
        <div class="form-group">
          <label for="receiverAccountNumber">Receiver Account Number:</label>
          <input type="text" id="receiverAccountNumber" v-model="receiverAccountNumber" required>
        </div>
        <button type="submit">Submit Donation</button>
      </form>
    </div>
  
  
  
    </AuthenticatedLayout>
    
  </template>

  <script setup>
  import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
  import { ref } from 'vue';

  </script>
  <style scoped>
  .donation-form {
    width: 600px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  .form-group {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
  }
  
  input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  select {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  option {
    background-color: #f5f5f5;
  }
  </style>
  