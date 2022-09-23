<script setup lang ="ts">
import ref from "@vue/reactivity";
import card from "./card.vue";

const maison = ref({});

const register = async (data) => {
  // Let's imagine this is a submit handler
  await new Promise((r) => setTimeout(r, 2000));
};
</script>

<template>

 

 <div class="p-2">

<h2 class="text-2xl">Résultat (Prévisualisation)</h2>
 <!-- Optionnel on affiche les données -->

<card v-bind="maison" />
 </div>

 <div class="m-40 p-1 border-cyan-900 border rounded">
 
<!-- On passe la "ref" à FormKit -->
 <FormKit type="form"

:submit-attrs="{ classes: { input: 'bg-red-500 m-5 p-1 rounded' } }"

 :config="{
 classes: {
        label: 'block mb-1 font-bold text-sm mx-5 text-3xl',
        input: 'mx-5 text-gray-800 mb-1 w-1/4 text-2xl rounded border-black shadow-md',
        help: 'mx-5 text-xs text-gray-500 text-2xl',
        message: 'mx-5 text-red-500 text-xs text-2xl',
        
 },
 }"
 v-model="maison"


    @submit="register"
  >
  
    <h2 class=" m-5 text-5xl">Formulaire d'ajout de maison</h2>
    <FormKit
      name="Adresse"
      label="Adresse"
      help="What is your Adresse ?"
      validation="required|Adresse"

    />

    <FormKit
      name="Nombre de M²"
      label="Nombre de M²"
      help="Quelle est votre surface ?"
      validation="required|Nombre de M²"

    />


    <FormKit
      name="Name"
      label="Name"
      help="Enter the Name"
      validation="required|length:3"
    />
    <FormKit
      name="Prix"
      label="Prix"
      help="Marqué le prix en Euro"

    />
  </FormKit>

 </div>
</template>


