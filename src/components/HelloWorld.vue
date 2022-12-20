<template>
  <div>
    <ul class="list-group">
      <li class="list-group-item" v-for="country in countries" v-bind:key="country.area">{{ country.name.common }}</li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return { countries: [] };
  },
  name: "HelloWorld",
  props: {
    msg: String,
  },
  mounted() {
    let global = this;
    axios
      .get("https://restcountries.com/v3.1/all")
      .then(function (response) {
        global.countries = response.data;
      })
      .catch(function (error) {
        console.log(error);
      });
  },
};
</script>
