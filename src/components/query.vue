<script setup>
import Options from "./options.vue";
</script>

<template>
  <div class="pb-4">
    <label class="pb-4 flex">Query type *</label>
    <div class="flex flex-col sm:flex-row gap-4 w-auto">
      <Options click="General Enquiry" />
      <Options click="Support Request" />
    </div>
  </div>
</template>
