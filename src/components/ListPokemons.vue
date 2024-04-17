<script setup>
const pokemon = defineProps(["name", "url"])

const idPokemon = pokemon.url.split('/')[6]
const imageUrl = "https://assets.pokemon.com/assets/cms2/img/pokedex/full/" + idPokemon.padStart(3, 0) + ".png"
</script>

<template>
    <div class="col-md-4 g-3">
        <div class="card">
            <img :src="imageUrl" class="card-img-top" alt="..." />
            <div class="card-body">
                <p class="card-title">
                    {{ pokemon.name }}
                </p>
                <a :href="pokemon.url" class="card-text">
                    {{ pokemon.url }}
                </a>
            </div>
        </div>
    </div>
</template>

<style></style>