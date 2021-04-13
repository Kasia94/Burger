<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->

    <Header style="border: 1px solid red" />
    <Burger />
    <Cost :ingredients="ingredients"/>
    <Ingredients :ingredients="ingredients" />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Burger from "./components/Burger.vue";
import Cost from "./components/Cost.vue";
import Header from "./components/Header.vue";
import Ingredients from "./components/Ingredients.vue";

export default {
  name: "App",
  components: {
    // HelloWorld
    Burger,
    Cost,
    Header,
    Ingredients,
  },
  data() {
    return {
      ingredients: [
        { name: "mięso", value: 0, price: 1.5 },
        { name: "ser", value: 0, price: 0.5 },
        { name: "sałata", value: 0, price: 0.2 },
        { name: "bekon", value: 0, price: 1.0 },
        { name: "pomidor", value: 0, price: 0.5 },
      ],
    };
  },
};
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
