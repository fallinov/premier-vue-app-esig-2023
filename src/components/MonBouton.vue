<script setup>
defineProps({
  couleur: {
    type: String,
    default: 'white'
  },
  texte: String
})
</script>

<template>
  <button :style="{ backgroundColor: couleur }">
    <em v-if="texte">{{ texte }}&nbsp;</em>
    <slot>Hello</slot>
  </button>
</template>

<style scoped>

</style>
