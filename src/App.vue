<template>
  <div id="app"><Companies /> <Staff /></div>
</template>

<script>
import Companies from "./components/Companies";
import Staff from "./components/Staff";

export default {
  name: "App",
  components: {
    Companies,
    Staff
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
