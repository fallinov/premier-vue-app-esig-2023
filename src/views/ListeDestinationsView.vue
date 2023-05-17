<script setup>

import CarteDestination from "@/components/CarteDestination.vue";
import MonBouton from "@/components/MonBouton.vue";
</script>

<template>
    <h1>{{ titre }}</h1>
    <mon-bouton couleur="red" texte="toto">Txtx</mon-bouton>
    <mon-bouton couleur="yellow">Titi</mon-bouton>
    <mon-bouton texte="Bonjour">Tutu</mon-bouton>
    <mon-bouton></mon-bouton>
    <MonBouton>blibla</MonBouton>
    <img class="logo" src="/favicon.ico" alt="Icone">
    <img class="logo" src="@/assets/logo.svg" alt="Logo">
    <div class="nos-destinations">
        <carte-destination
                v-for="destFor in destinations"
                :key="destFor.id"
                :dest="destFor"
        ></carte-destination>
    </div>
</template>

<style scoped>

</style>
