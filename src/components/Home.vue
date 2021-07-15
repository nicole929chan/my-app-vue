<template>
  <div class="home">
    home
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
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
      console.log('name.value: ' + name.value);
    }
    console.log('name.value: ' + name.value);
    return {
      name, age, handleClick
    }
  }
}
</script>
