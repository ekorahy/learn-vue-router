<script setup>
import sourceData from '@/data/locale/data.json'
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const destinationId = computed(() => parseInt(route.params.id))

const destination = computed(() => {
  return sourceData.destinations.find((dest) => dest.id === destinationId.value)
})
</script>

<template>
  <p v-if="!destination">Data not found</p>
  <section v-else>
    <h2>{{ destination.name }}</h2>
    <img :src="`/images/${destination.image}`" :alt="destination.name" />
    <p>{{ destination.description }}</p>
  </section>
</template>
