<template>
  <div class="contact">
    <form @submit="handleFormSubmit">
      <label for="firstName">First Name</label>
      <input type="text" id="firstName" placeholder="First Name" />
      <label for="lastName">Last Name</label>
      <input type="text" id="lastName" placeholder="Last Name" />
      <label for="Company Name">Company Name</label>
      <input type="text" id="Company Name" placeholder="Company Name" />
      <label for="email">Email</label>
      <input type="text" id="email" placeholder="email@email.com" />
      <label for="message">Message</label>
      <textarea type="text" id="message" placeholder="Message" />
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  methods: {
    handleFormSubmit(e: Event) {
      e.preventDefault();
      console.log(e);
    },
  },
});
</script>
