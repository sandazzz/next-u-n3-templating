<template>
    <div>
      <p>{{ state.someObject.name }}</p>
      <button @click="changeName">Changer le nom</button>
      <button @click="replaceObject">Remplacer l'objet</button>
    </div>
  </template>
  
  <script lang="ts" setup>
  import { reactive, watch } from 'vue';
  
  // Etat réactif
  const state = reactive({
    someObject: {
      name: 'Alice',
      age: 30
    }
  });
  
  // Utilisation de watch pour observer `state.someObject`
  watch(
    () => state.someObject,
    (newValue, oldValue) => {
      console.log('Ancienne valeur :', oldValue);
      console.log('Nouvelle valeur :', newValue);
    },
    { deep: true } // Observer toutes les propriétés de l'objet
  );
  
  // Fonction pour changer le nom dans l'objet
  function changeName() {
    state.someObject.name = 'Bob'; // Modifie une propriété interne
  }
  
  // Fonction pour remplacer complètement l'objet
  function replaceObject() {
    state.someObject = { name: 'Charlie', age: 25 }; // Remplace l'objet entier
  }
  </script>
  