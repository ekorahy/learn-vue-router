<script setup>
import sourceData from '@/data/locale/data.json'

const destinations = sourceData.destinations
</script>

<template>
  <h2>All Destination.</h2>
  <router-link v-for="destination in destinations" :key="destination.id" :to="destination.slug">
    <h3>{{ destination.name }}</h3>
    <img :src="`/images/${destination.image}`" :alt="destination.name" />
  </router-link>
</template>
