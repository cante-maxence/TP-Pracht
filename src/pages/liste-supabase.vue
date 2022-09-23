<script setup lang="ts">
import card from "../components/card.vue";
import {supabase} from "../supabase";
console.log("supabase :", supabase); // pour vérifier et "garder" supabase dans le code


let { data: Maison, error } = await supabase
.from("Maison")
.select("*")
const maisons = Maison ; 

console.log("Maison", Maison)
</script>

<template>
    <card v-for="maison in maisons" :key="maison.nomMaison" v-bind="maison"></card>
</template>