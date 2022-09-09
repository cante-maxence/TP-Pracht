<template>
    <div class="p-2">
        <h1 class="text-2xl">Liste pour v-for</h1>
        <div v-for="maisons in maisons" :key="maisons.prix">
            <card class="w-1/2" v-bind="maisons"/>
        </div>
    </div>
    </template>

<script setup lang="ts">
import card from "../components/card.vue";

const obj = {
  nom: "Maison bleu",
  prix: "5000",
};
import maisons from "../assets/maisons.json";
</script>