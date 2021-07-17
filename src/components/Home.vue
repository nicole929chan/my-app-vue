<template>
  <div class="home">
    home
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
    <input type="text" v-model="name">
    <button @click="age++">add 1 age</button>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
  name: 'Home',
  setup() {  
    const name = ref('mario')  // name.value = 'mario'
    const age = ref(34)        // age.value = 34
    const handleClick = () => {
      name.value = 'luigi'
      age.value = 30
    }
    return {
      name, age, handleClick
    }
  }
}
</script>
