<script lang="ts" setup>
import { ref,type Ref } from 'vue'
const count = ref(0)
const count2 = ref(0)
//passage de paramètres d'une valeur réactive à une fonction
//vue conserve la réactivité
const increment = (v:Ref<number>)=> v.value++
const incrementCounter = ()=> increment(count) 
const incrementCounter2 = ()=>increment(count2) 
</script>
<template>
  <div>count 1 : {{ count }}</div>
  <button @click="incrementCounter" type="button">Increment réactif 1</button>
  <div>count 2 : {{ count2 }}</div>
  <button @click="incrementCounter2" type="button">Increment réactif 2</button>
</template>
<style></style>
