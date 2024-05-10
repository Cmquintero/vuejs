<script setup>
import { ref } from 'vue';
const users= ["pepe", "Juana ", "Andrea", "lola"] 
const isChecked = ref(true);
</script>
<template>
    <ul>
        <li v-for="( user, index) in users" :key=" index ">{{ index }} {{ user }} </li>
    </ul>
    <input type="checkbox" id="check" v-model="isChecked"/>
    <label for="check"> Pick</label>
    <div class=" bg-blue-400  text-white rounded py-1 px-2 w-40 mx-auto" :class="{' bg-orange-400' : isChecked}">Este es un mensaje  </div>
    <div v-show="isChecked"> Este es un mensaje que se podria ocultar</div>
    <div v-if="isChecked">Este es otro mensaje que se podria ocultar </div>
    <div v-else> Este mensajesi se podria mostrar ya que cumple la condicion</div>
</template>