<script setup>
import { useRoute } from 'vue-router'
import NavigationList from '/src/components/molecules/NavigationList.vue'
const route = useRoute()
</script>

<template>
  <header>
    <router-link to="/">Vue School Travel App</router-link>
    <nav>
      <NavigationList />
    </nav>
  </header>
  <main><router-view :key="route.path"></router-view></main>
</template>
