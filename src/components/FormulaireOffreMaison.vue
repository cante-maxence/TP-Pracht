<script setup lang="ts">
import { ref } from "@vue/reactivity";
import card from "./card.vue";

const maison = ref({});

const register = async (data) => {
  // Let's imagine this is a submit handler
  await new Promise(r => setTimeout(r, 2000))
}
</script>

<template>

 

 <div class="p-2">

<h2 class="text-2xl">Résultat (Prévisualisation)</h2>
 <!-- Optionnel on affiche les données -->

<card v-bind="maison" />
 </div>

 <div class="m-7 p-1 border-cyan-900 border ">

<!-- On passe la "ref" à FormKit -->
 <FormKit type="form" 



 :config="{
 classes: {
        label: 'block mb-1 font-bold text-sm ',
        input: 'text-gray-800 mb-1 w-1/4 rounded border-black shadow-md',
        help: 'text-xs text-gray-500',
        message: 'text-red-500 text-xs',
 },
 }"
 v-model="maison"


    @submit="register"
  >
  
    <h2 class=" mx-5">Register</h2>
    <FormKit
      name="email"
      label="Email"
      help="What is your email address?"
      validation="required|email"
    />
    <FormKit
      name="password"
      label="Password"
      help="Enter your new account’s password"
      validation="required|length:6"
    />
    <FormKit
      name="password_confirm"
      label="Confirm password"
      help="Re-type that previous password"
      validation="required|confirm"
    />
  </FormKit>

 </div>
</template>


