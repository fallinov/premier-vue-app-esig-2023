<script setup>
defineProps({
    dest: {
        type: Object,
        required: true
    }
})
</script>

<template>
    <div class="destination">
        <h2>{{ dest.nom }}</h2>
        <div class="prix">Prix: {{ dest.prix }} CHF</div>
        <p>{{ dest.description }}</p>
    </div>
</template>

<style scoped lang="scss">
.destination {
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 1rem;
    max-width: 340px;
    background: linear-gradient(180deg, #fff, #efefef);

    h2 {
        margin: 0 0 .1em;
    }

    .prix {
        font-weight: bold;
        margin-bottom: .5em;
    }

    p {
        margin: .75em 0;
        line-height: 1.5;
    }
}
</style>
