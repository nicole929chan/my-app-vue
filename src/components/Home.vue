<template>
  <div class="home">
    home
    <p>My name is {{ name }} and my age is {{ age }}</p>
  </div>
</template>

<script>
export default {
  name: 'Home',
  setup() {  // run first
    
    let name = 'mario'
    let age = 34
    // 看起來與 data() 很像, 但是目前為止的差異是
    // setup()的變數是不可互動, data()的變數可互動
    return {
      name,
      age
    }
  },
  created() {  // run second
  },
  mounted() {  // run third
  }
}
</script>
