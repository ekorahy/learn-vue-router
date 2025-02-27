<script setup>
import navigations from '@/data/constans/navigations'
import NavigationItem from '../atoms/NavigationItem.vue'
</script>

<template>
  <ul>
    <li v-for="navigation in navigations" :key="navigation.id">
      <NavigationItem :name="navigation.name" :path="navigation.path" />
    </li>
  </ul>
</template>
