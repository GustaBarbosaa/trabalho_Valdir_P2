<script setup>
    const personagem = defineProps(["name", "url", "status", "species", "gender", "location", "image", "episode"])

</script>

<template>
    <div class="col-md-3">
        <div class="card mb-3 p-3">
            <img :src="personagem.image" class="card-img-top" alt="...">
            <div class="card-body">
                <p class="card-title"><b>Nome:</b> {{ personagem.name }}</p>
                <p class="card-title"><b>Status: </b>
                <font style="background-color: green;" v-if="personagem.status === 'Alive'" color="white">{{ personagem.status }}</font>
                <font style="background-color: yellow;" v-else-if="personagem.status === 'unknown' "color="white">{{ personagem.status }}</font>
                <font style="background-color: red;"v-else color="white">{{ personagem.status }}</font></p>
                <p class="card-title"><b>Espécie:</b> {{ personagem.species }}</p>
                <p class="card-title"><b>Gênero:</b> {{ personagem.gender }}</p>
                <p class="card-title"><b>Localização Atual:</b> {{ personagem.location.name }}</p>
                <p class="card-title"><b>Episódios:</b> {{ personagem.episode.length }}</p>
                
            </div>
        </div>
    </div>
</template>

<style>

</style>