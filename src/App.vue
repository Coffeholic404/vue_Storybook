<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.svg" />
    <LimitedInput />
  </div>
</template>

<script setup>
import LimitedInput from './components/LimitedInput.vue'
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
