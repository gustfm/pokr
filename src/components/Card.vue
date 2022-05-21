<template>
  <div class="card-container">
    <div class="card-content">
      <div class="card-number-tip left-tip">
        <p>{{ value }}</p>
      </div>
      <h1>{{ value }}</h1>
      <div class="card-number-tip right-tip">
        <p>{{ value }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
export default class Card extends Vue {
  @Prop({ required: true }) public readonly value!: number;
}
</script>

<style scoped>
.card-container * {
  cursor: pointer;
}
.card-container {
  background-color: #20272d;
  border: 3px solid #2e373e;
  width: 58px;
  height: 83px;
  border-radius: 6px;
  margin: 5px 3px;

  display: flex;
  justify-content: center;
  align-items: center;
}
.card-container:hover {
  border: 3px solid #5830bc;
}
.card-container:hover > .card-content {
  background-color: #5830bc;
}
.card-content {
  background-color: #2e373e;
  width: 44px;
  height: 68px;
  border-radius: 4px;

  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}
h1 {
  margin: 0;
  padding: 0;
  font-size: 24pt;
  color: #e8eef4;
}
.card-number-tip {
  position: absolute;
  font-size: 7pt;
  font-weight: 600;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background-color: #20272d;
  color: #ffffff;

  display: flex;
  justify-content: center;
  align-items: center;
}
.left-tip {
  top: -4px;
  left: -4px;
}
.right-tip {
  bottom: -4px;
  right: -4px;
}
p {
  margin: 0;
}
</style>
