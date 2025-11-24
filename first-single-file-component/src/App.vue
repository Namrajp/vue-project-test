<script setup>
import { ref } from "vue";

// const titleClass = ref("title");
const titleId = ref("title");
</script>

<template>
  <h1 :id="titleId">Make me red</h1>
  <!-- add dynamic class binding here -->
</template>

<style>
#title {
  color: red;
}
</style>
