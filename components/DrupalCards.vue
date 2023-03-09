<template>
    <div>
        <h2>Cards from Drupal headless</h2>
        <div class="cards-container">
            <DrupalCard v-for="card in cards" :key="card.id" :card="card">
            </DrupalCard>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
import { restConfig, siteDomain } from '@/src/App'


export default {
    name: 'DrupalCards',
    data() {
        return {
            cards: []
        }
    },
    async fetch() {
        this.cards = await axios.get(siteDomain + '/cards', restConfig).then(response => response.data)
    },

}

</script>