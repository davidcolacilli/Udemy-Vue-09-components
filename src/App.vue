<template>
  <div id="app-container">
    <header-component heading="Plans"/>
    <plans/>
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
  margin-top: 60px;
}
</style>
