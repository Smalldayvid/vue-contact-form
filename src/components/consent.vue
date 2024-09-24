<template>
  <div class="pb-4 flex gap-4 items-center">
    <input
      id="check"
      type="checkbox"
      class="cursor-pointer"
      :checked="modelValue"
      @change="emitInput"
    />
    <label for="check" class="select-none"
      >I support to being contacted by the team *</label
    >
  </div>
</template>

<script setup>
import { defineEmits, defineProps } from "vue";

defineProps({
  modelValue: Boolean,
});

const emit = defineEmits(["update:modelValue"]);

const emitInput = (event) => {
  emit("update:modelValue", event.target.checked);
};
</script>
