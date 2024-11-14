<script setup>
import { ref, watch } from 'vue'
const numbers = ref([])

watch(numbers, () => console.log('new number added'))
watch(numbers, (nouValor, anticValor) => console.log(nouValor, anticValor));

const randomNum = () => numbers.value.push(Math.random())
</script>
<template>
  <button @click="randomNum">Add Random Number</button>
</template>
