<script setup>
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'

// Importe ref depuis vue
import {reactive, ref} from 'vue'
import CarteDestination from "@/components/CarteDestination.vue";
import MonBouton from "@/components/MonBouton.vue";

const titre = ref('Destinations de vacances')
const destinations = reactive([
    {
        id: 1,
        nom: 'Malaga',
        prix: 890,
        description: 'Malaga est une ville du sud de l\'Espagne, sur la Costa del Sol, connue pour ses plages et ses stations balnéaires.'
    },
    {
        id: 2,
        nom: 'Honolulu',
        prix: 3890,
        description: 'Honolulu est la capitale et la plus grande ville de l\'État d\'Hawaï, aux États-Unis. Située sur la côte sud de l\'île d\'Oahu, elle est le centre des affaires, du commerce et du divertissement d\'Hawaï.'
    },
    {
        id: 3,
        nom: 'Oslo',
        prix: 1290,
        description: 'Oslo, la capitale et la plus grande ville de Norvège, est située à la pointe sud du fjord d\'Oslo. Entourée de collines verdoyantes et de forêts, elle possède de nombreux parcs et espaces verts.'
    },
    {
        id: 4,
        nom: 'Bora-Bora',
        prix: 5490,
        description: 'Bora-Bora est une petite île volcanique de l\'archipel de la Société en Polynésie française. Entourée d\'un lagon et d\'une barrière de corail, elle est célèbre pour ses plages de sable blanc bordées de cocotiers et ses bungalows sur pilotis.'
    },
    {
        id: 5,
        nom: 'Paris',
        prix: 590,
        description: 'Paris, capitale de la France, est une grande ville européenne et un centre mondial de l\'art, de la mode, de la gastronomie et de la culture. Son paysage urbain du XIXe siècle est traversé par de larges boulevards et la Seine.'
    },
    {
        id: 6,
        nom: 'Londres',
        prix: 490,
        description: 'Londres, la capitale de l\'Angleterre et du Royaume-Uni, est une ville moderne dont l\'histoire remonte à l\'époque romaine. En son centre se dressent l\'imposant Parlement, l\'emblématique Big Ben et l\'abbaye de Westminster, lieu de couronnement des monarques britanniques.'
    }
])
</script>

<template>
    <h1>{{ titre }}</h1>

    <!-- Menu de navigation -->
    <nav>
      <router-link to="/">Accueil</router-link>
      -
      <router-link to="/about">A propos</router-link>
        -
      <router-link to="/destinations">Nos destinations</router-link>
    </nav>
    <!-- Emplacement ou sera affiché le composant de la route -->
    <RouterView />

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

<style scoped lang="scss">
/*
Pour installer sass/scss :
npm install -D sass
*/
h1 {
  text-align: center;
}

.logo {
  display: block;
  margin: 0 auto;
  max-width: 125px;
}

.nos-destinations {
  margin: 2rem auto 1rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1em;
}

</style>
