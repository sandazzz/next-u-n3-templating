<template>
    <div class="anounce">
      <h5>{{ title }}</h5>
      <p>{{ description }}</p>
    </div>
    <hr v-if="!isLast" />
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

defineProps<{
  title: string;
  description: string;
  isLast: boolean;
}>();
</script>

