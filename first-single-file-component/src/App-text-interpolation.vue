<script setup>
import { ref } from "vue";
import { reactive } from "vue";
// component logic
// declare some reactive state here.
const message = ref("Hello World!");
console.log(message);
message.value = "new value";

const counter = reactive({
  count: 0,
});
counter.count++;
console.log(counter.count);
</script>

<template>
  <h1>{{ message.split(" ").reverse().join("") }}</h1>
  <p>Count is: {{ counter.count }}</p>
</template>

<style scoped></style>
