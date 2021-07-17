<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Reactivity</h2>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjOne">click me</button>
    <p>{{ nameTwo }}</p>
  </div>
</template>

<script>
import { reactive } from '@vue/reactivity'
export default {
  name: 'Home',
  setup() {  
    const ninjaOne = reactive({ name: 'mario', age: 30})
    let nameTwo = reactive('Dior')

    const updateNinjOne = () => {
      nameTwo = "Fendi"            // 不會改變其值
      nameTwo = reactive('Fendi')  // 這樣也不會改變
    }

    return {
      ninjaOne, updateNinjOne, nameTwo
    }
  }
}
</script>
