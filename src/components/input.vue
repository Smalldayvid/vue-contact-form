<script setup>
import { defineProps } from "vue";

defineProps({
  label: {
    type: String,
    default: "First Name",
  },
});
</script>

<template>
  <div class="flex flex-col">
    <label>{{ label }} *</label>
    <input
      class="rounded-md border border-[#87a3a6] focus:border-[#87a3a6] focus:border-2 px-2 py-1"
    />
  </div>
</template>
