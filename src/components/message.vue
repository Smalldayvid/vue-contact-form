<script setup>
import { defineEmits, defineProps } from "vue";

defineProps({
  label: {
    type: String,
    default: "Message",
  },
  modelValue: String,
});

const emit = defineEmits(["update:modelValue"]);

const emitInput = (event) => {
  emit("update:modelValue", event.target.value);
};
</script>

<template>
  <div class="pb-4">
    <label>{{ label }} *</label>
    <div>
      <textarea
        class="rounded-md border border-[#87a3a6] focus:border-[#87a3a6] focus:border-2 py-1 px-2 w-full"
        :value="modelValue"
        @input="emitInput"
      ></textarea>
    </div>
  </div>
</template>
