<script setup>
import { ref } from 'vue';
import IMG from '../assets/img/img_0.png';

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <div className="products-container">
    <div className="product-img"></div>
    <div className="product-slider"></div>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
