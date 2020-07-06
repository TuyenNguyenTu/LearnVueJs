<template>
  <div id="app">
    <b-container class="bv-example-row">
      <img alt="Vue logo" src="./assets/logo.png" />
      <HelloWorld msg="Welcome to Your Vue.js App" />
      <RoadMapComponent></RoadMapComponent>
    </b-container>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import RoadMapComponent from "./components/RoadMap.Component";
export default {
  name: "App",
  components: {
    HelloWorld,
    RoadMapComponent,
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
