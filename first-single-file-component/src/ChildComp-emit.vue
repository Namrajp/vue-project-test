<script setup>
    // declare emitted events
    const emit = defineEmits(['response'])

    // emit with argument
    emit('response', 'hello from child')
</script>

<template>
  <p>A Child Component is here inside parent Comp!</p>
</template>