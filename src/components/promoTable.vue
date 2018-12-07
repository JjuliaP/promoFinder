<template>
  <div>
    <table @promos="this.promos">
      <thead>
        <tr>
          <th>Promo</th>
          <th>Description</th>
        </tr>
      </thead>
      <tr v-for="code in Object.keys(promos)">
        <td>{{code}}</td>
        <td>{{promos[code]}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "promoTable",
  props: { promos: Object }
  //   data() {
  //     return {
  //       //   promos: {
  //       //     groupon: {
  //       //       "kohls.com": [{ CODE1: "DESCRIPTION1" }, { CODE2: "DESCRIPTION2" }],
  //       //       "ebay.com": [] // no codes
  //       //     },
  //       //     honey: {
  //       //       "kohls.com": [{ CODE3: "DESCRIPTION3" }, { CODE4: "DESCRIPTION4" }],
  //       //       "ebay.com": [] // no codes
  //       //     }
  //       //   }
  //       promos: {
  //         qq: "111",
  //         ww: "222"
  //       }
  //     };
  //   }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>