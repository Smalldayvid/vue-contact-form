<script setup>
import Input from "./input.vue";
</script>

<template>
  <form>
    <section class="pb-4">
      <div class="flex flex-col sm:flex-row w-full gap-4 pb-4">
        <Input label="First Name" />
        <Input label="Last Name" />
      </div>
      <Input label="Email Address" />
    </section>
  </form>
</template>
