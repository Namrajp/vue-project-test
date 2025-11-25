<script setup>
import { ref, watch } from 'vue'

let count = ref(0)
const message = ref("Hello World!");

watch(count, (newCount) => {
  // yes, console.log() is a side effect
  
  console.log(`new count is: ${newCount}`)
})
count.value++
count.value++
count.value++
</script>
<template>
    <p> {{ count }}</p>
</template>