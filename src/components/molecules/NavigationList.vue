<script setup>
import sourceData from '@/data/locale/data.json'
const destinations = sourceData.destinations

import NavigationItem from '../atoms/NavigationItem.vue'
</script>

<template>
  <ul>
    <li v-for="navigation in destinations" :key="navigation.id">
      <NavigationItem :name="navigation.name" :id="navigation.id" :slug="navigation.slug" />
    </li>
  </ul>
</template>
