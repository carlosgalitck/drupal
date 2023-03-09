<template>
    <div>
        <img :src="image.field_media_image[0].url" alt="card-image">
    </div>
</template>

<script>
import axios from 'axios'
import { restConfig, siteDomain } from '@/src/App'

export default {
    name: 'MediaImage',
    props: ['media'],
    data() {
        return {
            image: []
        }
    },
    async fetch() {
        this.image = await axios.get(siteDomain + '/media/' + this.media + '/edit', restConfig).then(response => response.data)
    },
}

</script>
