<script setup>
import { ref, reactive } from 'vue'
const name = ref()
const state = reactive({ age: null })
const ceo = ref('Mark')
const week = ref("Tueday")
const countries = ref([
  "Thai","Malaysia","Singapore"
])
</script>

<template>
  <nav>
    <h3>Home page</h3>
    <div v-for="(country,index) in countries" :key="index">
     {{ index + 1 }} - {{ country }}
    </div>
    <hr />
    <span>
      {{
      week == 'Monday' ? 'If executed'
      : week == 'Tueday' ? 'Else If1 executed'
      : week == 'Wednesday' ? 'Else If2 executed'
      : 'Else executed'
      }}
    </span>
    <hr />
    <span v-if="ceo == 'Jhon'">
      If condition is executed
    </span>

    <span v-else-if="ceo == 'Elon'">
      Else If condition is executed
    </span>

    <span v-else="ceo == 'Mark'">
      Else condition is executed
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