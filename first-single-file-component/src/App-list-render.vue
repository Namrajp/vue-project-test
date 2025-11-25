<script setup>
    import {ref} from 'vue'
    let id = 0

    let text = ref("")
    // const todo = ref("Hello vue")
    const todos = ref([
        { id: id++, text: "build in python"},
        {id: id++, text: "mvc in asp.net"},
        {id: id++, text: "go to nature"}
    ])
    // const todos = ["do yoga", "call employer", "go to nature"]
</script>

<template>
    <input v-model = "text" placeholder=""></input>
    <p> {{  text }}</p>
    <ul>
        <li v-for = "todo in todos"> {{ todo.text }}</li>
    </ul>
</template>