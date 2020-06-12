<template>
  <div id="app-container">
    <plan v-for="pla in plans" :name="pla.name" :price="pla.price" :key="pla.name"/>
  </div>
</template>

<script>
import Plan from './components/Plan.vue'

export default {
  name: 'App',
  components: {
    Plan
  },
  data() {
    return {
      plans: [
        {
          name: 'Beginner',
          price: 2
        },
        {
          name: 'Intermediate',
          price: 4
        },
        {
          name: 'Advanced',
          price: 6
        },
        {
          name: 'Pro',
          price: 10
        },
      ]
    }
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
