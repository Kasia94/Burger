<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    
    <Header style="border: 1px solid red" />
    <Burger/>
    <Cost/>
    <Ingredients/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Burger from './components/Burger.vue'
import Cost from './components/Cost.vue'
import Header from './components/Header.vue'
import Ingredients from './components/Ingredients.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Burger,
    Cost,
    Header,
    Ingredients
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
