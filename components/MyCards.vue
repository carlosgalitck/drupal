<template>
    <div>
        <h2>Cards from External API</h2>
        <div class="cards-container">
            <MyCard v-for="planet in planets" :key="planet.title" :planet="planet">
            </MyCard>
        </div>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'MyCards',
    data() {
        return {
            planets: []
        }
    },
    async fetch() {
        this.planets = await axios.get('https://api.nuxtjs.dev/planets').then(response => response.data)
    },

}

</script>