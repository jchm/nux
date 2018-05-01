<template>
    <div>
	<h1>{{ photo.title }}</h1>
        <img :src="photo.url">
    </div>
</template>

<script>
import axios from 'axios'

export default {
  asyncData ({ params, error }) {
    return axios.get('https://jsonplaceholder.typicode.com/photos/' + params.id)
    .then((res) => {
      return { photo: res.data }
    })
    .catch((e) => {
      error({ statusCode: 404, message: 'Photos not found' })
    })
  }   
}
</script>

<style scoped></style>
