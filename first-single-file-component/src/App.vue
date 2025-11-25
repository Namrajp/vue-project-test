<script setup>
import { ref } from 'vue'
import ChildComp from './ChildComp-emit.vue'

const childMsg = ref('No child msg yet')
</script>

<template>
  <ChildComp @response="(msg) => childMsg = msg"/>
  <p>{{ childMsg }}</p>
</template>