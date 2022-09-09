

<script setup>
import card from "../components/card.vue";

const obj = {
  nom: "Maison bleu",
  prix: "5000",
};
</script>


<template>

<card nom="grgrgr rgre" prix="8" adresse="8 rue bidon" />
<card v-bind="obj"/>
</template>