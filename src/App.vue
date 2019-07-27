<template>
  <div id="app">
    <employee-page />
  </div>
</template>

<script>
import EmployeePage from "./components/pages/EmployeePage";
export default {
  name: "app",
  components: {
    EmployeePage
  }
};
</script>

<style>
@font-face {
  font-family: "RobotoLight";
  src: url("/assets/fonts/Roboto-Light.ttf") format("truetype");
}

html,
body,
#app {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
  font-family: "RobotoLight", sans-serif;
}
</style>
