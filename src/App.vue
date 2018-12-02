<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <promoInput 
        label="Enter merchant here" 
        placeholder="ebay.com"
    />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import promoInput from "./components/promoInput.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    promoInput
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
