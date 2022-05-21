<template>
  <div class="voting-task-container">
    <a href="#" class="sentence">{{ value }}</a>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

import Card from "@/components/Card.vue";

@Component({
  components: {
    Card,
  },
})
export default class Sentence extends Vue {
  @Prop() public readonly value!: string;
}
</script>

<style scoped>
.voting-task-container .sentence {
  font-size: 30pt;
  color: #ffffff;
}
</style>
