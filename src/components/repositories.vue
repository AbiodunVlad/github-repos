<template>
  <div>
    <h1 class="title">Get GitHub Repositories</h1>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "repositories-github",
  data() {
    return {
      repos: null,
    };
  },
  created: function () {
    axios
      .get("https://api.github.com/users/abiodunvlad/repos")
      .then((response) => {
        this.repos = response.data;
      });
  },
};
</script>

<style>
body {
  font: 15px/1.8 "Poppins", sans-serif !important;
}
.table td,
.table th {
  padding: 20px !important;
}
</style>
