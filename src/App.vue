<script setup>
import { reactive } from "vue";
import { useToast } from "vue-toastification";

import Button from "@/components/Button.vue";
import Consent from "@/components/consent.vue";
import Message from "@/components/message.vue";
import Input from "./components/input.vue";
import Option from "./components/Option.vue";

const initialForm = {
  firstName: "",
  lastName: "",
  email: "",
  message: "",
  tC: false,
};

const form = reactive(initialForm);

const toast = useToast();

const handleSubmit = () => {
  if (!form.tC) {
    toast.error("Agree to T and C first");
  } else {
    toast.success("Message sent!");
  }

  const data = {
    firstName: form.firstName,
    lastName: form.lastName,
    email: form.email,
    message: form.message,
    tC: form.tC,
  };

  console.log(data);

  // Object.assign(form, initialForm);
  Object.keys(form).forEach((key) => {
    form[key] = key === "tC" ? false : ""; // Reset to initial values
  });
};
</script>

<template>
  <main class="w-full h-screen flex items-center justify-center bg-green-100">
    <div class="bg-white rounded-lg shadow-lg p-5 w-auto">
      <h1 class="font-bold text-xl py-4 select-none">Contact Us</h1>
      <section class="pb-4">
        <div class="flex flex-col sm:flex-row w-full gap-4 pb-4">
          <Input v-model="form.firstName" label="First Name" />
          <Input v-model="form.lastName" label="Last Name" />
        </div>
        <Input v-model="form.email" type="email" label="Email Address" />
      </section>

      <div class="pb-4">
        <label class="pb-4 flex">Query type *</label>
        <div class="flex flex-col sm:flex-row gap-4 w-auto">
          <Option id="general" text="General Enquiry" />
          <Option id="support" text="Support Request" />
        </div>
      </div>

      <Message v-model="form.message" />
      <Consent v-model="form.tC" />
      <Button @click="handleSubmit">Submit</Button>
    </div>
  </main>
</template>
