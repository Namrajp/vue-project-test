<script setup>
import { ref } from 'vue'
import ChildComp from './ChildCompProp.vue'

const greeting = ref('Hello from parent')
</script>

<template>
  <ChildComp :msg="greeting" />
  <!-- A child component can accept input from the parent via props. -->
</template>