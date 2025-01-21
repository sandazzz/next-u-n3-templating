<script lang="ts" setup>
import { reactive, computed } from 'vue'

const author = reactive({
  name: 'John Resig',
  posts: [
    'IA - Innovation',
    'OLLAMA and Vue-js - LLM in Frontend',
    'RAG - LLM with MONGODB store'
  ]
})

// a computed ref
const publishedPostsMessage = computed(() => {
  return author.posts.length > 0 ? 'Yes' : 'No'
})
const publishedPostMessageWithoutComputed = ()=>{
  return author.posts.length > 0 ? 'Yes' : 'No'
}
const addPost = ()=>{
  author.posts.push("Foo IA - Foo IA")
}
const removePost = ()=>{
  author.posts.pop()
}
// récuperation de la valeur via .value
console.log(publishedPostsMessage.value)
</script>
<template>
  <button @click="addPost">addPost</button>
  <button @click="removePost">removePost</button>
  <p>Has published posts:</p>
  <span>{{ publishedPostsMessage }}</span>
  <span>without computing : {{publishedPostMessageWithoutComputed()}}</span>
</template>