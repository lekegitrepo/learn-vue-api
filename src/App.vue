<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <ApiReference msg="Welcome to Your Vue.js App" />
</template>

<script>
import ApiReference from "./components/api-reference.vue";

export default {
  name: "App",
  components: {
    ApiReference,
  },
  data: () => ({
    model: 0,
    colors: ["primary", "secondary", "yellow darken-2", "red", "orange"],
  }),
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
