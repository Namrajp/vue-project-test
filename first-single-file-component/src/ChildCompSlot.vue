<script setup>
    const props = defineProps({
    msg: String
    })
</script>
<template>
  <p>A Child Component is here inside parent Comp!</p>

  <h3>{{  msg }}</h3>
<!-- in child template -->
<slot/>
</template>

