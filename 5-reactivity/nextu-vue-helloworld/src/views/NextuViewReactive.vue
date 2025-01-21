<script lang="ts" setup>
import { reactive } from 'vue'
const org = {
  nested: { count: 0 },
  arr: ['foo', 'bar']
}
const obj = reactive(org)
function mutateDeeply() {
  // these will work as expected.
  obj.nested.count++
  obj.arr.push('baz')
}
/**
 * seulement le proxy est réactif, 
 * les mutations sur l'objet original ne déclenche 
 * pas la mise à jour du DOM
 */
function mutateDeeplyOrig() {
  // these will work as expected.
  org.nested.count++
  org.arr.push('baz')
}
</script>
<template>
  <button @click="mutateDeeply">Ajouter de nouveau un element baz dans le tableau</button>  
  <div v-for="(item,i) in obj.arr" :key="i">
    {{item}}
  </div>
  <br/>
  <div>Objet Orignal {{org.nested.count}}</div>
  <button @click="mutateDeeplyOrig">Ajouter de nouveau un element baz dans le tableau original</button>  
  <div v-for="(itemOrg,i) in org.arr" :key="i">
    {{itemOrg}}
  </div>
</template>