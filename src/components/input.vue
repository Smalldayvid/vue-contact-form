<script setup>
import { defineEmits, defineProps } from "vue";

defineProps({
  label: {
    type: String,
    default: "First Name",
  },
  type: {
    type: String,
    default: "text",
  },
  modelValue: String,
});

const emit = defineEmits(["update:modelValue"]);

const emitInput = (event) => {
  emit("update:modelValue", event.target.value);
};
</script>

<template>
  <div class="flex flex-col">
    <label>{{ label }} *</label>
    <input
      class="rounded-md border border-[#87a3a6] focus:border-[#87a3a6] focus:border-2 px-2 py-1"
      :type="type"
      :value="modelValue"
      @input="emitInput"
    />
  </div>
</template>
