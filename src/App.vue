<template>
  <div id='app'>
    <img alt="Vue logo" src="./assets/logo.png">
    <promoInput label="Enter merchant here" placeholder="ebay.com" autofocus=true></promoInput>
    <br>
    <promoBtn label="Search"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import promoInput from "./components/promoInput.vue";
import promoBtn from "./components/promoBtn.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    promoInput,
    promoBtn
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
