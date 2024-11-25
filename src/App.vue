<script setup>
import ProductList from './components/ProductList.vue'
</script>

<template>
  <div class="container">
    <h1>Ürün Listesi</h1>
    <ProductList />
  </div>
</template>

<style>
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

h1 {
  color: #2c3e50;
  text-align: center;
  margin-bottom: 2rem;
}
</style>