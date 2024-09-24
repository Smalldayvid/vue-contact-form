<script setup>
import { defineProps } from "vue";
import { useToast } from "vue-toastification";

defineProps({
  text: {
    type: String,
    default: "Submit",
  },
});

const toast = useToast();
</script>

<template>
  <button
    @click="
      () => {
        toast.success('Message Sent!');
      }
    "
    class="border-none rounded-md bg-[#0c7d69] hover:bg-[#2b4246] py-2 w-full text-white justify-items-center"
  >
    {{ text }}
  </button>
</template>
