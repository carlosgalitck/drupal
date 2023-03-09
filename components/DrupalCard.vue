<template>
    <div class="drupal-card">
        <div class="card-image">
            <MediaImage :key="card.image" :media="card.image"></MediaImage>
        </div>
        <div class="card-title">
            <h2>{{ card.title }}</h2>
        </div>

        <div class="card-description">
            <p>{{ card.description }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DrupalCard',
    props: ['card']
}

</script>

<style>
@import '~/assets/css/card.css';
</style>