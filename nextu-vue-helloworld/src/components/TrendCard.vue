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

defineProps<{
  avatar: string
  username: string
  description: string
}>()
</script>
