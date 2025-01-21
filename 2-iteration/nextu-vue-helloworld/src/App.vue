<script setup lang="ts">
import type { Product } from './models/product'
import ProductListView from './views/ProductListView.vue'
const productsData: Product[] = [
  { id: '1', label: 'Camembert', description: 'Le meilleur camembert de France', qte: 12 },
]
</script>
<template>
  <ProductListView :products="productsData" />
</template>
<style scoped></style>
