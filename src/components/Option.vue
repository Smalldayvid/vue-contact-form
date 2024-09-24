<script setup>
import { defineProps } from "vue";

defineProps({
  text: {
    type: String,
    default: "General Enquiry",
  },
  id: String,
});
</script>

<template>
  <div class="w-full">
    <input :id="id" type="radio" name="anything" class="peer hidden" />
    <label
      :for="id"
      class="border border-gray-500 px-6 py-2 rounded-lg w-full cursor-pointer peer-checked:border-green-500 peer-checked:bg-green-600/10"
    >
      {{ text }} *
    </label>
  </div>
</template>
