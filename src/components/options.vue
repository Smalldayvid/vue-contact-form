<script setup>
import { defineProps } from "vue";

defineProps({
  click: {
    type: String,
    default: "General Enquiry",
  },
});
</script>

<template>
  <div
    class="flex flex-row gap-4 items-center cursor-pointer hover:border-[#dff1e7] hover:bg-green-600/20 hover:border-2 rounded-md border border-[#87a3a6] px-3 py-1 w-auto"
  >
    <input
      type="radio"
      class="hover:bg-green-600/60 cursor-pointer hover:border-4 hover:border-green-600/20"
    />
    <span>{{ click }} *</span>
  </div>
</template>
