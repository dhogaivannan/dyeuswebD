<template>
  <div>
    <div class="flex-container">
      <div class="item selected">Details</div>
      <div class="item">How to make it</div>
      <div class="item">Ingredients</div>
    </div>
    <div class="information">
      <div>
        An amino acid found in tea, L-theanine is similar to glutamic acid, an
        excitatory neurotransmitter found in the central nervous system. A
        precursor to acetylcholine
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "detail",
};
</script>

<style scoped>
.flex-container {
  padding: 1em 1em;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
}
.item {
  padding: 1em;
  font-size: 16px;
  line-height: 21px;
}
.selected {
  font-weight: bold;
  border-bottom: 3px solid #f8d702;
}
.information {
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 28px;
  color: rgba(29, 41, 26, 0.8);
  margin: 0 24px 0 38px;
}
</style>
