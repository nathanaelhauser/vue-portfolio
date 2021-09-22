<template>
  <div class="portfolio">
    <h1>This is the portfolio page</h1>

    <!-- Setup a loop of Planets -->
    <div class="planets">
      <Card />
      <Planet fill="green" />
      <Planet fill="red" />
      <Planet fill="blue" />
      <Planet fill="#4DA6FF" />
      <Planet :radius="700" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Card from "@/components/Card.vue";
import Planet from "@/components/Planet.vue";

export default defineComponent({
  components: { Card, Planet },
});
</script>

<style scoped>
.cards {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
</style>
