<template>
  <div class="poker-container flex flex-col items-center justify-center h-full">
      <Sentence value="DASH-2222" />
      <CardsContainer />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import CardsContainer from "@/views/CardsContainer.vue";
import Sentence from "@/views/Sentence.vue";

@Component({
  components: {
    CardsContainer,
    Sentence,
  },
})
export default class PokerContainer extends Vue {}
</script>
