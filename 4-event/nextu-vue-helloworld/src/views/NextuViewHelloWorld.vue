<script lang="ts" setup>
import { ref } from 'vue'
const themes: string[] = [
    "Les algorithmes font-ils la loi ?",
    "Tu veux dévélopper des web components ? Pas d'inquiétude utilise vue-js",
    "L'ia c'est l'avenir !",
    "Bienvenue chez webtech ?"
];
const theme = ref(themes[0])
const updateTheme = ()=>{
    // Génère un index aléatoire entre 0 et la longueur du tableau
    const randomIndex = Math.floor(Math.random() * themes.length);
    console.log(randomIndex);
    theme.value = themes[randomIndex];  
}
const save = ()=>{
  console.log("parent call");
}
const saveName = (name:string,event:Event)=>{
 console.log(`Hi ${name}`);
 event.stopPropagation(); // empêche la propagation de l'évènement vers le conteneur

}  
</script>
<template>
  <div>{{ theme }}</div>
  <button @click="updateTheme" type="button">Modifier le message</button>

  <div @click="save()">
   <button @click="saveName('André', $event)">Save</button>
  </div>
</template>
<style></style>
