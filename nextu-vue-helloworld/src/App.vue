<script setup lang="ts">
//import type { Product } from './models/product'
import AsideView from './components/layouts/AsideView.vue'
import HeaderView from './components/layouts/HeaderView.vue'
import NavView from './components/layouts/NavView.vue'
import HomeProjectView from './views/HomeProjectView.vue'
//import NextuViewHelloWorld from './views/NextuViewHelloWorld.vue'
//import ProductListView from './views/ProductListView.vue'
/**const productsData: Product[] = [
  { id: '1', label: 'Camembert', description: 'Le meilleur camembert de France', qte: 12 },
]**/
</script>
<template>
  <AsideView />
  <main>
    <HeaderView />
    <NavView />
    <HomeProjectView />
  </main>
</template>
<style scoped></style>
