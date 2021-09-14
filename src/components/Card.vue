<template>
  <div
    class="card"
    :style="{ backgroundImage: `url(${imgSrc})` }"
    @mouseenter="handleMouseEnter"
    @mouseleave="handleMouseLeave"
  >
    <div class="card-content hidden">
      <h3>{{ title }}</h3>
      <p>{{ technology }}</p>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    imgSrc: {
      default: "https://source.unsplash.com/random/400x300",
      type: String,
    },
    imgAlt: {
      default: "An Image",
      type: String,
    },
    title: {
      default: "Card Title",
      type: String,
    },
    technology: {
      default: "JavaScript",
      type: String,
    },
    description: {
      default:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatibus!",
      type: String,
    },
  },
  methods: {
    handleMouseEnter(e: Event) {
      const target = e.target as HTMLDivElement;
      if (target && target.children.length) {
        target.children[0].className = "card-content";
      }
    },
    handleMouseLeave(e: Event) {
      const target = e.target as HTMLDivElement;
      if (target && target.children.length) {
        target.children[0].className = "card-content hidden";
      }
    },
  },
});
</script>

<style scoped>
button {
  border: none;
  padding: 0;
  margin: 0;
  background-color: transparent;
}
.card {
  width: 400px;
  height: 300px;
}
.card-content {
  background-color: rgba(255, 255, 255, 0.5);
  position: absolute;
  width: 400px;
  height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.card-content h3 {
  margin: 0;
}
.card-content p {
  margin: 0 1em 1em 1em;
}
.hidden {
  visibility: hidden;
}
.cover {
  width: 400px;
  height: 300px;
  position: absolute;
  z-index: 2;
}
</style>
