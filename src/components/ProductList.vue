<script setup>
import { ref } from 'vue'

const products = ref([
  {
    id: 1,
    name: 'Akıllı Telefon',
    price: 12999,
    image: '/images/phone.jpg',
    description: 'Son model akıllı telefon'
  },
  {
    id: 2,
    name: 'Laptop',
    price: 24999,
    image: '/images/laptop.jpeg',
    description: 'Yüksek performanslı dizüstü bilgisayar'
  },
  {
    id: 3,
    name: 'Tablet',
    price: 8999,
    image: '/images/tablet.jpg',
    description: 'Hafif ve taşınabilir tablet'
  },
  {
    id: 4,
    name: 'Akıllı Saat',
    price: 3999,
    image: '/images/smartwatch.jpg',
    description: 'Spor ve günlük kullanım için akıllı saat'
  }
])
</script>

<template>
  <div class="products-grid">
    <div v-for="product in products" :key="product.id" class="product-card">
      <img :src="product.image" :alt="product.name">
      <div class="product-info">
        <h2>{{ product.name }}</h2>
        <p class="description">{{ product.description }}</p>
        <p class="price">{{ product.price.toLocaleString('tr-TR') }} ₺</p>
        <button class="buy-button">Sepete Ekle</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 2rem;
  padding: 1rem;
}

.product-card {
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  transition: transform 0.2s;
  background: white;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

.product-card:hover {
  transform: translateY(-5px);
}

.product-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.product-info {
  padding: 1rem;
}

.product-info h2 {
  margin: 0;
  font-size: 1.25rem;
  color: #2c3e50;
}

.description {
  color: #666;
  font-size: 0.9rem;
  margin: 0.5rem 0;
}

.price {
  font-size: 1.25rem;
  font-weight: bold;
  color: #2c3e50;
  margin: 0.5rem 0;
}

.buy-button {
  width: 100%;
  padding: 0.5rem;
  background-color: #42b883;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s;
}

.buy-button:hover {
  background-color: #3aa876;
}
</style>