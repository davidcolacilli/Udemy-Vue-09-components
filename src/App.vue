<template>
  <div id="app-container">
    <header-component heading="asdfg"/>
    <plans/>
    <p></p>
  </div>
</template>

<script>
import Plans from './components/Plans.vue'
import HeaderComponent from './components/HeaderComponent.vue'

export default {
  name: 'App',
  components: {
    Plans,
    HeaderComponent
  }
}
</script>

<style>
#app-container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin: 60px auto 0;
  max-width: 800px;
}
</style>
