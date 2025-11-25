<script setup>
    import {ref} from 'vue'
    let id = 0

    let newTodo = ref("")
    // const todo = ref("Hello vue")
    const todos = ref([
        { id: id++, text: "build in python"},
        {id: id++, text: "mvc in asp.net"},
        {id: id++, text: "go to nature"}
    ])

    function addTodo() {
        todos.value.push({id: id++, text: newTodo.value})
        newTodo.value = ""
    }
    function removeTodo(todo) {
        todos.value = todos.value.filter((doit) => doit !== todo)
    }
    // const todos = ["do yoga", "call employer", "go to nature"]
</script>

<template>
    <form action="" @submit.prevent = "addTodo">
        <input v-model = "newTodo" placeholder=""></input>
        <button>Add todo</button>
    </form>
    <p> {{  text }}</p>
    <ul>
        <li v-for = "todo in todos"> 
            {{ todo.text }}
            <button @click = "removeTodo(todo)">Remove todo</button>
        </li>
    </ul>
</template>