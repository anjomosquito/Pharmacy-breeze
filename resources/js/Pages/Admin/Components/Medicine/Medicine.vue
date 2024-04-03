
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
    <Head title="Medicine" />
    <AuthenticatedLayout>
    <div class="addmed-form">
      <h1>Add Medicine</h1>
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
          <label for="quantity">Quantity</label>
          <input type="text" id="quantity" v-model="quantity">
        </div>
        <div class="form-group">
          <label for="dosage">Dosage</label>
          <input type="text" id="dosage" v-model="dosage" required>
        </div>
        <div class="form-group">
          <label for="expdate">Exp Date:</label>
          <input type="text" id="expdate" v-model="expdate" required>
        </div>
        <div class="form-group">
          <label for="amount">Donation Amount:</label>
          <input type="number" id="amount" v-model.number="amount" required min="1">
        </div>
        <div class="form-group">
          <label for="paymentMethod">Payment Method:</label>
          <select id="paymentMethod" v-model="paymentMethodd" required>
            <option value="gcash">GCash</option>
            <option value="paypal">PayPal</option>
            <option value="paymaya">PayMaya</option>
          </select>
        </div>
        <div class="form-group">
          <label for="receiverAccountNumber">Receiver Account Number:</label>
          <input type="text" id="receiverAccountNumber" v-model="receiverAccountNumber" required>
        </div>
        <button type="submit">Add to Inventory</button>
      </form>
    </div>
  
  
  
    </AuthenticatedLayout>
    
  </template>

  <script setup>
  import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
  import { ref } from 'vue';

  </script>
  <style scoped>
  .addmed-form {
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
  