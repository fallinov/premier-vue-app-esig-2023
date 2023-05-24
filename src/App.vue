<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
 <header>
  <div class="logo">Démo Vue Router</div>
  <nav>
   <RouterLink exact-active-class="actif" to="/">Accueil</RouterLink>
   <RouterLink exact-active-class="actif" to="/contact">Nous contacter</RouterLink>
   <RouterLink exact-active-class="actif" :to="{ name: 'fiche', params: { nom: 'Jean' }}">Fiche client Jean</RouterLink>
   <RouterLink exact-active-class="actif" to="/fiche/Pauline">Fiche client Pauline</RouterLink>
  </nav>
 </header>
 <main>
  <RouterView />
 </main>
</template>

<style scoped lang="sass">
header
 padding: 1rem
 background-color: ghostwhite
 .logo
  font-size: 1.5rem
  font-weight: bold
 nav
  margin-top: 1rem
  a
   margin-right: 1rem
   text-decoration: none
   color: lightseagreen
  a.actif
   color: darkorange

main
 padding: 1rem
 border: 4px solid ghostwhite
</style>
