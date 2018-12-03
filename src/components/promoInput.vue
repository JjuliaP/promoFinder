<template>
  <div>
    <label for="input">{{ label }}</label>
    <input
      type="text"
      name="gender"
      id="input"
      :placeholder="this.placeholder"
      :autofocus="this.autofocus"
      v-model="email"
    >
    <button @click="submit">click me!!</button>
  </div>
</template>

<script>
export default {
  name: "promoInput",
  props: {
    label: String,
    placeholder: String,
    autofocus: String //Boolean
  },
  data() {
    return {
      email: "https://jsonplaceholder.typicode.com/posts/42"
    };
  },
  methods: {
    submit() {
      fetch(this.email, {
            method: 'GET',
            headers: {
                credentials: 'include',
                accept:
                    "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8",
                "upgrade-insecure-requests": 1
        }
      })
        .then(response => response.json())
        .then(result => alert(result));
      //alert(this.email);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
