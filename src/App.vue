<template>
  <div id="app">
    <Repository />
  </div>
</template>

<script>
import repositories from "./components/repositories";
export default {
  name: "App",
  components: {
    repositories,
  },
};
</script>
