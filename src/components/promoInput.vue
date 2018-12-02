<template>
  <div>
    <label for="input">{{ label }}</label>
    <input type="text" name="gender" id="input" :placeholder="this.placeholder">
  </div>
</template>

<script>
export default {
  name: "promoInput",
  props: {
    label: String,
    placeholder: String,
    focus: Boolean
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
