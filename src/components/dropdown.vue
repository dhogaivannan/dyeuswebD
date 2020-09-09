<template>
  <div class="aselect" :data-value="value" :data-list="list">
    <div class="selector" @click="toggle()">
      <div class="label">
        <span>Qty: {{ value }}</span>
      </div>
      <div class="arrow" :class="{ expanded: visible }"></div>
      <div :class="{ hidden: !visible, visible }">
        <ul>
          <li
            :key="item"
            :class="{ current: item === value }"
            v-for="item in list"
            @click="select(item)"
          >{{ item }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "aselect",
  data: () => ({
    value: 1,
    list: [1, 2, 3, 4],
    visible: false,
  }),
  methods: {
    toggle() {
      this.visible = !this.visible;
    },
    select(option) {
      this.value = option;
    },
  },
};
</script>

<style lang="scss" scoped>
.aselect {
  margin: 10px 30px;
  .selector {
    border: 1px solid gainsboro;
    border-radius: 8px;
    background: #f8f8f8;
    position: relative;
    z-index: 1;
    .arrow {
      position: absolute;
      right: 10px;
      top: 40%;
      width: 0;
      height: 0;
      border-left: 7px solid transparent;
      border-right: 7px solid transparent;
      border-top: 10px solid #888;
      transform: rotateZ(0deg) translateY(0px);
      transition-duration: 0.3s;
      transition-timing-function: cubic-bezier(0.59, 1.39, 0.37, 1.01);
    }
    .expanded {
      transform: rotateZ(180deg) translateY(2px);
    }
    .label {
      font-family: "Inter";
      font-style: normal;
      padding: 20px 0 21px 20px;
      display: block;
      color: #1d291a;
      padding: 12px;
      font-size: 16px;
      font-weight: 600;
      font-size: 16px;
      line-height: 19px;
    }
  }
  ul {
    width: 100%;
    list-style-type: none;
    padding: 0;
    margin: 0;
    font-size: 16px;
    border: 1px solid gainsboro;
    position: absolute;
    border-radius: 8px;
    z-index: 1;
    background: #fff;
  }
  li {
    padding: 12px;
    color: #666;

    &:hover {
      color: white;
      background: seagreen;
    }
  }
  .current {
    background: #eaeaea;
  }
  .hidden {
    visibility: hidden;
  }
  .visible {
    visibility: visible;
  }
}
</style>
