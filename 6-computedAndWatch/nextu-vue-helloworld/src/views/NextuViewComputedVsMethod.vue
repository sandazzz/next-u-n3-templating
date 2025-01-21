<template>
    <div>
      <p>Nom complet (computed): {{ fullNameComputed }}</p>
      <p>Nom complet (computed): {{ fullNameComputed }}</p>
      <p>Nom complet (méthode): {{ fullNameMethod() }}</p>
      <p>Nom complet (méthode): {{ fullNameMethod() }}</p>
      <button @click="changeName">Changer le prénom</button>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, computed } from 'vue';
  
  // Variables réactives
  const firstName = ref('Alice');
  const lastName = ref('Smith');
  
  // Propriété calculée (computed)
  const fullNameComputed = computed(() => {
    console.log('Calcul de fullName (computed)');
    return `${firstName.value} ${lastName.value}`;
  });
  
  // Méthode (fonction)
  function fullNameMethod() {
    console.log('Calcul de fullName (méthode)');
    return `${firstName.value} ${lastName.value}`;
  }
  
  // Fonction pour changer le prénom
  function changeName() {
    firstName.value = 'Bob';
  }
  </script>
  