<template>
  <svg :width="diameter" :height="diameter">
    <defs>
      <pattern
        id="image"
        x="0"
        y="0"
        patternUnits="userSpaceOnUse"
        :width="diameter"
        :height="diameter"
      >
        <image
          x="0"
          y="0"
          xlink:href="https://source.unsplash.com/random/400x300"
        ></image>
      </pattern>
    </defs>
    <circle
      :cx="radius"
      :cy="radius"
      :r="planetRadius"
      :stroke="borderColor"
      stroke-width="3"
      :fill="fill"
    />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    radius: {
      default: 100,
      type: Number,
    },
    borderColor: {
      default: "black",
      type: String,
    },
    fill: {
      default: "url(#image)",
      type: String,
    },
  },
  computed: {
    diameter() {
      return 2 * this.radius;
    },
    planetRadius() {
      return Math.floor(this.radius * 0.8);
    },
  },
});
</script>
