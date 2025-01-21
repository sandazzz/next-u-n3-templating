<template>
    <div class="anounce">
      <h5>{{ title }}</h5>
      <p>{{ description }}</p>
    </div>
    <hr v-if="!isLast" />
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

// Définir les props avec leurs types
defineProps<{
  title: string;
  description: string;
  isLast: boolean; // Indique si c'est le dernier élément
}>();
</script>

