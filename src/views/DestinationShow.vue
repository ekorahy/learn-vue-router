<script setup>
import { ref } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const destination = ref(null)

const fetchData = async () => {
  try {
    const response = await fetch(`https://travel-dummy-api.netlify.app/${route.params.slug}.json`)
    destination.value = await response.json()
  } catch (error) {
    console.error('Error fetching data:', error)
    destination.value = null
  }
}

fetchData()
</script>

<template>
  <p v-if="!destination">Data not found</p>
  <section v-else>
    <h2>{{ destination.name }}</h2>
    <img :src="`/images/${destination.image}`" :alt="destination.name" />
    <p>{{ destination.description }}</p>
  </section>
</template>
