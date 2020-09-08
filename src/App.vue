<template>
  <div id="app">
    <dropdown />
    <cart-b />
    <buy-t />
    <detail />
  </div>
</template>

<script>
import Detail from "./components/main.vue";
import cartB from "./components/addtocart.vue";
import buyT from "./components/save.vue";
import dropdown from "./components/dropdown.vue";
export default {
  name: "app",
  components: {
    Detail,
    cartB,
    buyT,
    dropdown,
  },
};
</script>

<style>
#app {
  font-family: "DM Sans";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
body {
  margin: 0px;
}
</style>
