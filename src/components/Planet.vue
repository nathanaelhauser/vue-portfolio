<template>
  <div :style="planetStyle"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    radius: {
      default: 100,
      type: Number,
    },
    backgroundImage: {
      default: "https://source.unsplash.com/random/400x300",
      type: String,
    },
    backgroundRepeat: {
      default: "no-repeat",
      type: String,
    },
    backgroundSize: {
      default: "cover",
      type: String,
    },
    borderColor: {
      default: "black",
      type: String,
    },
    borderStyle: {
      default: "solid",
      type: String,
    },
    borderWidth: {
      default: "thick",
      type: String,
    },
  },
  data() {
    const sideLength = this.radius * 2;

    return {
      planetStyle: {
        "background-image": `url(${this.backgroundImage})`,
        "background-repeat": this.backgroundRepeat,
        "background-size": this.backgroundSize,
        "border-radius": `${this.radius}px`,
        "border-color": this.borderColor,
        "border-style": this.borderStyle,
        "border-width": this.borderWidth,
        width: `${sideLength}px`,
        height: `${sideLength}px`,
      },
    };
  },
});
</script>
