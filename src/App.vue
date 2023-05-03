<script setup>
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'

// Importe ref depuis vue
import {ref} from 'vue'
import CarteDestination from "@/components/CarteDestination.vue";

const titre = ref('Destinations de vacances')
const destinations = ref([
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
  <!--  <header>

      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

      <div class="wrapper">
          <h1>Hello afasfd</h1>
        <HelloWorld msg="You did it!" />

        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
        </nav>
      </div>
    </header>

    <RouterView />-->
    <h1>{{ titre }}</h1>
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

.nos-destinations {
  margin: 2rem auto 1rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1em;
}

</style>
