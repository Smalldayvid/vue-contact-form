<script setup>
import { defineProps } from "vue";

defineProps({
  label: {
    type: String,
    default: "Message",
  },
});
</script>

<template>
  <div class="pb-4">
    <label>{{ label }} *</label>
    <div>
      <textarea
        class="rounded-md border border-[#87a3a6] focus:border-[#87a3a6] focus:border-2 py-1 px-2 w-full"
      ></textarea>
    </div>
  </div>
</template>
