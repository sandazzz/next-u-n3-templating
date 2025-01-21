<template>
  <div class="trend">
    <figure>
      <img class="avatar" :src="avatar" alt="avatar" />
    </figure>
    <div class="trend-details">
      <h6>{{ username }}</h6>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

// Définir les props avec leurs types
defineProps<{
  avatar: string
  username: string
  description: string
}>()
</script>
