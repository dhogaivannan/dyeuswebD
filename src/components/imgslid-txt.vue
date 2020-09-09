<template>
  <div class="common">
    <div class="viewer">
      <img :src="image" />
    </div>
    <div class="control">
      <div
        class="dot"
        :key="i"
        v-for="(item, i) in menu"
        @click="changeActive(i)"
        :class="{ active: i === cursor }"
      >
        {{ i }}
      </div>
    </div>
    <div class="slider">
      <img
        width="70"
        :src="menu[i]"
        :key="i"
        v-for="(item, i) in menu"
        @click="changeActive(i)"
        :class="{ active: i === cursor }"
      />
    </div>

    <div class="text">Sunshine Bliss Daily Vitamin D</div>
  </div>
</template>

<script>
export default {
  name: "imgtext",
  methods: {
    changeActive(i) {
      console.log(i);
      this.cursor = i;
    },
  },
  data: () => ({
    menu: [
      "https://picsum.photos/id/1/400/400",
      "https://picsum.photos/id/2/400/400",
      "https://picsum.photos/id/3/400/400",
      "https://picsum.photos/id/5/400/400",
    ],
    cursor: 0,
  }),
  computed: {
    image() {
      return this.menu[this.cursor];
    },
  },
};
</script>

<style lang="scss" scoped>
.control {
  /* bottom: 10px; */
  margin: 10px;
  left: 0;
  right: 0;
  text-align: center;
  .dot {
    transition: all 0.4s;
    text-indent: -9999px;
    width: 11px;
    height: 11px;
    display: block;
    border-radius: 10px;
    background: #062744;
    opacity: 0.2;
    display: inline-block;
    cursor: pointer;
    &.active {
      opacity: 1;
      width: 24px;
      opacity: 1;
      background: #f8d702;
    }
  }
  .dot + .dot {
    margin-left: 0.3rem;
  }
}
.text {
  margin: 15px;
  padding: 0 24px;
  font-style: normal;
  font-weight: bold;
  font-size: 28px;
  line-height: 36px;
  text-align: center;
  color: #1d291a;
}
* {
  margin: 0;
  padding: 0;
}
body {
  background: #ccc;
}
.viewer {
  display: flex;
  justify-content: space-around;

  img {
    border-radius: 8px;
  }
}
.slider {
  display: flex;
  justify-content: space-around;

  img {
    border-radius: 8px;
    border: 3px solid #ffffff;
    filter: drop-shadow(0px 3px 10px rgba(0, 0, 0, 0.11));
  }
  .active {
    border: 3px solid #f8d702;
  }
}
</style>
