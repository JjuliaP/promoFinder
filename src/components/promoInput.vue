<template>
  <div>
    <label for="input">{{ label }}</label>
    <input type="text" :placeholder="this.placeholder" :autofocus="this.autofocus" v-model="email">
    <button @click="fetchData">Search</button>
    <br>

    <table align="center" :style="this.style">
      <thead>
        <tr>
          <th>Promo</th>
          <th>Description</th>
        </tr>
      </thead>
      <tr v-for="code in Object.keys(resultObject)">
        <td>{{code}}</td>
        <td>{{resultObject[code]}}</td>
      </tr>
    </table>
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
  //   computed: {
  //     style: function() {
  //       return {};
  //     }
  //   },
  data() {
    return {
      email: "https://jsonplaceholder.typicode.com/todos/1",
      resultObject: {},
      style: {
        display: "none"
      }
    };
  },
  methods: {
    fetchData() {
      return fetch(this.email)
        .then(response => response.json())
        .then(json => {
          this.resultObject = json;
          this.style.display = !!this.resultObject ? "table" : "none";
        });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
