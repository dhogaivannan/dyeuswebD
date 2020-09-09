<template>
  <div id="app">
    <img-t />
    <star-b />
    <div class="price">$ 13.99</div>
    <radio-b />
    <dropdown />
    <cart-b />
    <buy-t />
    <detail />
  </div>
</template>

<script>
import Detail from "./components/details.vue";
import cartB from "./components/addtocart.vue";
import buyT from "./components/save.vue";
import dropdown from "./components/dropdown.vue";
import radioB from "./components/radiobuttons.vue";
import starB from "./components/rating.vue";
import imgT from "./components/imgslid-txt.vue";
export default {
  name: "app",
  components: {
    Detail,
    cartB,
    buyT,
    dropdown,
    radioB,
    starB,
    imgT,
  },
};
</script>

<style>
#app {
  padding: 20px 20px;
  font-family: "DM Sans";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  justify-content: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 500px;
}
body {
  margin: 0px;
}
@media (min-width: 30em) and (orientation: landscape) {
  #app {
    margin: 20px 30%;
  }
}
.price {
  font-style: normal;
  font-weight: 500;
  font-size: 36px;
  line-height: 47px;
  margin-top: 10px;
  text-align: center;

  color: #1d291a;
}
</style>
