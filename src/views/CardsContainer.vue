<template>
  <div class="cards-container">
    <Card :value="0" />
    <Card :value="2" />
    <Card :value="3" />
    <Card :value="5" />
    <Card :value="8" />
    <Card :value="13" />
    <Card :value="20" />
    <Card :value="40" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import Card from "@/components/Card.vue";

@Component({
  components: {
    Card,
  },
})
export default class CardsContainer extends Vue {}
</script>

<style scoped>
.cards-container {
  /* width: 70%; */

  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width: 600px;
  height: 200px;
  /* display: grid;
    grid-template-columns: auto auto auto auto auto auto auto auto;
    grid-template-rows: 1; */
}
</style>
