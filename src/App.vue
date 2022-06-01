<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <MyCounter />
  <RandomFox />
</template>

<script>
import MyCounter from "./components/MyCounter.vue";
import RandomFox from "./components/RandomFox.vue";
// Global CSS
import "./assets/main.css";

export default {
  name: "App",
  components: {
    MyCounter,
    RandomFox,
  },
};
</script>

<style>
* {
  background-color: black;
  color: white;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
