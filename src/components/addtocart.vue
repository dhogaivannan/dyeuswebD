<template>
  <div>
    <div class="button">
      <div class="info">Add to Cart</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "cartbutton",
};
</script>

<style scoped>
.button {
  background: #32c574;
  box-shadow: 0px 0px 10px rgba(50, 197, 116, 0.59);
  border-radius: 8px;
  margin: 30px 30px;
  padding: 16px 0 15px 0;
}
.info {
  font-weight: bold;
  font-size: 22px;
  line-height: 29px;
  text-align: center;
  color: #ffffff;
  text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.15);
}
</style>
