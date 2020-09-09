<template>
  <div class="radiob">
    <label for="accessible">
      <input type="radio" value="accessible" name="quality" id="accessible" />
      <div class="info">
        <div>30 Gummies - $10</div>
      </div>
    </label>

    <label for="pretty">
      <input type="radio" value="pretty" name="quality" id="pretty" />
      <div class="info">
        <div class="right">
          <div>90 Gummies - $20</div>
          <div class="smtext">
            <div>List Price :<span class="offer"> USD 30</span></div>
            <div class="save">Save $10</div>
          </div>
        </div>
      </div>
    </label>

    <label for="accessible-and-pretty">
      <input
        type="radio"
        value="pretty"
        name="quality"
        id="accessible-and-pretty"
        checked
      />
      <div class="info">
        <div class="right">
          <div>Monthly subscription</div>
          <div class="smtext">
            <div class="save">Save 20%</div>
          </div>
        </div>
      </div>
    </label>
  </div>
</template>

<script>
export default {
  name: "radiobutton",
};
</script>

<style scoped>
.save {
  color: #32c574;
}
.right {
  width: 100%;
}
.smtext {
  display: flex;
  justify-content: space-between;
  font-style: normal;
  font-weight: bold;
  font-size: 12px;
  line-height: 2;
  color: rgb(170, 171, 172);
}
.info {
  display: flex;
  align-items: center;
  padding: 0 20px;
  margin: 10px 0px;
  font-weight: 500;
  font-style: normal;
  font-size: 18px;
  color: #000000;
}
[type="radio"] {
  border: 0;
  clip: rect(0 0 0 0);
  height: 2px;
  overflow: hidden;
  padding: 0;
  width: 1px;
  display: none;
}

label {
  margin-top: 12px;
  padding: 10px 3px;
  display: block;
  cursor: pointer;
  font-size: 1.5em;
  border-radius: 8px;
  background: rgba(240, 240, 240, 0.7);
}

[type="radio"] + .info:before {
  content: "";
  display: inline-block;
  width: 0.5em;
  height: 0.5em;
  border-radius: 0.5em;
  border: 0.125em solid #fff;
  box-shadow: 0 0 0 0.15em #949fa7;
  margin-right: 0.75em;
  transition: 0.5s ease all;
}

[type="radio"]:checked + .info:before {
  background: #32c574;
  box-shadow: 0 0 0 0.1em #32c574;
}

[type="radio"]:checked + label:before {
  background: #32c574;
  box-shadow: 0 0 0 0.1em #32c574;
}

.radiob {
  padding: 10px 30px;
}
.offer {
  text-decoration: line-through;
}
</style>
