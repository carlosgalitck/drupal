<template>
    <div class="card">
        <div class="card-front">
            <div class="card-image">
                <img :src="planet.image" />
            </div>
            <div class="card-title">
                <h2>{{ planet.title }}</h2>
            </div>
        </div>
        <div class="card-back">
            <div class="card-description">
                <p>{{ planet.description }}</p>
            </div>
            <div class="card-see-more">
                <a :href="'/planet/' + planet.slug">See more</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyCard',
    props: ['planet']
}

</script>

<style>
@import '~/assets/css/card.css';
</style>