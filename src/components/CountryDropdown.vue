<template>
  <div>country(data) 是一個 ref 物件</div>
  <select @change="changed" ref="country">
    <option value="">Please choose</option>
    <option value="UK">United Kingdom</option>
    <option value="US">America</option>
    <option value="In">India</option>
  </select>
</template>

<script>
export default {
  data() {
    return {
      country: ''
    }
  },
  mounted() {
    // 整個<select>...</select> DOM元素
    console.log(this.$refs.country);
  },
  methods: {
    changed() {
      // select DOM 元素所選中的值
      this.$emit('changed', this.$refs.country.value)
    }
  }
}
</script>