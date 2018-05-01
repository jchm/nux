<template>
    <div>
	<router-link v-for="photo in photos.slice(0, 100)" :key="photo.id" :to="{ name: 'photos-id', params: {id: photo.id}}">
            <img :src="photo.thumbnailUrl">
        </router-link>
    </div>
</template>

<script>
import axios from 'axios'
export default {
  asyncData ({ params, error }) {
    return axios.get('https://jsonplaceholder.typicode.com/photos')
    .then((res) => {
      return { photos: res.data }
    })
    .catch((e) => {
      error({ statusCode: 404, message: 'Photos not found' })
    })
  }   
}
</script>

<style scoped>
div {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-gap: 1em;
    padding: 1em;
}

img {
   width: 100%;
}

a:first-child {
 grid-column: span 2;
 grid-row: span 2;
}
</style>
