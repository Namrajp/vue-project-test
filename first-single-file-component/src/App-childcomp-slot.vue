<script setup>
import { ref } from 'vue'
import ChildComp from './ChildCompSlot.vue'

const msg = ref('from parent')
</script>

<template>
  <ChildComp>
      This is some slot content!
      Message: {{ msg }}
  </ChildComp>
</template>