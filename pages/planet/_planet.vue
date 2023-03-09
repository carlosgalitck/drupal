<template>
    <div class="container">
        <div class="planet-title">
            <h1 class="home-title">{{ planet.title }}</h1>
        </div>
        <div class="planet-image">
            <img :src="planet.image" />
        </div>
        <div class="planet-desc">
            <p>{{ planet.description }}</p>
        </div>
    </div>
</template>
  
<script>
import axios from 'axios'

export default {
    data() {
        return {
            planet: []
        }
    },
    async fetch() {
        this.planet = await axios.get('https://api.nuxtjs.dev/planets/' + this.$route.params.planet).then(response => response.data)
    },

}
</script>
  
<style>
@import '~/assets/css/planet.css';
</style>