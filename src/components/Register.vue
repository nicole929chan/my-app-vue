<template>
  <h1>Register...</h1>
  <CountryDropdown @changed="changeCountry" />
</template>

<script>
import CountryDropdown from './CountryDropdown.vue'

export default {
  components: {
    CountryDropdown
  },
  data() {
    return {
      form: {
        name: '',
        country: ''
      }
    }
  },
  methods: {
    changeCountry(value) {
      // value is from CountryDropdown component
      this.form.country = value
    }
  }
}
</script>