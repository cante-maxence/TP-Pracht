<template>
    <figure class="flex.flex-col m-3 border-1 p-2 bg-white rounded-sm">
        <img class="w-full h-auto object-cover rounded-t-lg"
            src="../assets/maison.png"
            alt="Maison BS"
            />
        <figcaption class="relative p-5 pt-8 border-2 border-t-0 rounded-lg border-indigo-100 flex flex-col">

            <div class="text-xl font-bold text-left text-indigo-500">{{prix}} $</div>
            <div class="text-gray-500 text-base inline-block">/month</div>
            <h3 class="text-xl text-gray-900">{{nom}}</h3>
            <div class="text-gray-500">{{adresse}}</div>
            <hr class="m-4 border-indigo-100" />
            <div class="flex flex-row justify-between text-sm">
                <div class="w-max"><beds class="h-5 w-5 mr-1 inline-block"/>{{lit}}</div>
                <div class="w-max"><bath class="h-5 w-5 mr-1 inline-block"/>{{baignore}}</div>
                <div class="w-max"><carre class="h-5 w-5 mr-1 inline-block"/>{{taille}}</div>
            </div>
            <div class="absolute top-7 right-7 border-2 border-indigo-100 w-10 h-10 grid place-items-start rounded-full">
                <heart/>
            </div>
        </figcaption>
    </figure>
</template>

<script>
import beds from "./icons/beds.vue";
import bath from "./icons/bath.vue";
import carre from "./icons/carre.vue";
import heart from "./icons/heart.vue";
export default {
  components: { carre, bath, beds, heart },

  props: {
    nomMaison: String,
    prix: Number,
    adresse: String,
    favori: Boolean,
    image: String, // les images sont simplement l'URL absolue (depuis la racine, débute par '/' )
    nbrSDB: Number,
    nbrChambres: Number,
  },
};
</script>
