<template>
  <div class="home">
    home
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
  name: 'Home',
  setup() {  
    let name = 'mario'
    let age = 34
    const p = ref("hello")  // 設定p的初始值, p.value = "hello"  不是<p>的內文

    const handleClick = () => {
      p.value.classList.add("text-primary")
      p.value.textContent = "inner text has changed..."
    }

    return {
      name, age, handleClick, p
    }
  }
}
</script>
