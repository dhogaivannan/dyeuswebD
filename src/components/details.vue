<template>
  <div>
    <div class="flex-container">
      <div
        :key="i"
        v-for="(item, i) in header"
        @click="changeActive(i)"
        :class="{ item, selected: i === cursor }"
      >
        {{ item }}
      </div>
    </div>
    <div class="information">
      <div class="back">
        <span v-if="!readMoreActivated">{{ text[cursor] }}</span>
        <div class="hide" v-if="!readMoreActivated" @click="activateReadMore">
          Read
        </div>
        <span v-if="readMoreActivated">{{ text[cursor] }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "readmore",
  methods: {
    changeActive(i) {
      this.cursor = i;
    },
    activateReadMore() {
      this.readMoreActivated = true;
    },
  },
  data() {
    return {
      text: [
        "An amino acid found in tea, L-theanine is similar to glutamic acid, an excitatory neurotransmitter found in the central nervous system. A precursor to acetylcholine",
        "An amino acid found in tea, L-theanine is similar to glutamic acid, an excitatory neurotransmitter found in the central nervous system. A precursor to acetylcholine added for how to take it placeholder",
        "An amino acid found in tea, L-theanine is similar to glutamic acid, an excitatory neurotransmitter found in the central nervous system. A precursor to acetylcholine added for ingredients placeholder",
      ],
      cursor: 0,
      header: ["Details", "How to take it", "Ingredients"],
      readMoreActivated: false,
    };
  },
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
.back {
  /* backdrop-filter: blur(2px); */
  background: linear-gradient(rgba(255, 255, 255, 0) 0%, #ffffff 49.09%);
}
.hide {
  text-align: right;
  margin-right: 20px;
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 21px;
  color: #2f80ed;
}
</style>
