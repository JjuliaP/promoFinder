<template>
  <div>
    <label for="input">{{ label }}</label>
    <input
      type="text"
      name="gender"
      id="input"
      :placeholder="this.placeholder"
      :autofocus="this.autofocus"
    >
  </div>
</template>

<script>
export default {
  name: "promoInput",
  props: {
    label: String,
    placeholder: String,
    autofocus: String //Boolean
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
