<script setup>
import { ref } from 'vue'
import { onMounted } from 'vue';

const pElementRef = ref(null)

onMounted(() => {
    // component is now mounted
    pElementRef.value.textContent = "I can modify DOM myself in this line! Hurray!!!"
})
</script>

<template>
  <p ref="pElementRef">Hello</p>
</template>