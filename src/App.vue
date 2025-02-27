<script setup>
import NavigationList from '/src/components/molecules/NavigationList.vue'
</script>

<template>
  <header>
    <router-link to="/">Vue School Travel App</router-link>
    <nav>
      <NavigationList />
    </nav>
  </header>
  <main><router-view></router-view></main>
</template>
