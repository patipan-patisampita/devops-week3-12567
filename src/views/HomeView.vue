<script setup>
import { ref, reactive } from 'vue'
const name = ref()
const state = reactive({ age: null })
const ceo = ref('Mark')
</script>

<template>
  <nav>
    <h3>Home page</h3>
    <span v-if="ceo == 'Jhon'">
      {{ ceo }}
    </span>

    <span v-else="ceo == 'Mark'">
      {{ ceo }}
    </span>

    <p>Name: {{ name }} Age: {{ state.age }}</p>
    Name:<input type="text" v-model="name">
    Age:<input type="text" v-model="state.age">
  </nav>
</template>

<style scoped>
nav {
  padding: 10px;
  text-align: center;
}
</style>