<script setup>
import Consent from "@/components/consent.vue";
import Contact from "@/components/contact.vue";
import Message from "@/components/message.vue";
import Query from "@/components/query.vue";
import Submit from "@/components/submit.vue";
</script>

<template>
  <main class="w-full h-screen flex items-center justify-center bg-green-100">
    <div class="bg-white rounded-lg shadow-lg p-5 w-auto">
      <h1 class="font-bold text-xl py-4 select-none">Contact Us</h1>
      <Contact />
      <Query />
      <Message />
      <Consent />
      <Submit text="Submit" />
    </div>
  </main>
</template>
