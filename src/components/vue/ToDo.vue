<script setup>
import { ref } from 'vue';
const todos = ref(['Estudiar bastante' ])
const todo = ref('')
function add() {
todos.value.unshift(todo.value)
todo.value=''
}
</script>
<template>
    <div class=" py-6 px-5 rounded shadow bg-slate-300 max-w-96 mx-auto mt-10">
        <div>
            <input v-model="todo" class=" px-3  w-4/5 outline-none rounded " />
            <button @click="add" class=" w-1/5 bg-green-400 text-white text-center">+</button>
        </div>
        <div 
        v-for=" (todo, i) in todos"
        :key="i"
        class=" px-1  mt-3 bg-orange-300 rounded text-center ">{{ todo}}</div>
    </div>
</template>