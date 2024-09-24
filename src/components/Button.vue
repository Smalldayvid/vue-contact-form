<script setup>
import { defineEmits, defineProps } from "vue";

defineProps({
  text: {
    type: String,
    default: "Submit",
  },
});

const emit = defineEmits(["click"]);

const handleClick = () => {
  emit("click");
};
</script>

<template>
  <button
    @click="handleClick"
    class="border-none rounded-md bg-[#0c7d69] hover:bg-[#2b4246] py-2 w-full text-white justify-items-center"
  >
    <slot />
  </button>
</template>
