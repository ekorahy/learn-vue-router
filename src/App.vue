<script setup>
import NavigationList from '/src/components/molecules/NavigationList.vue'
</script>

<template>
  <header>
    <nav>
      <NavigationList />
    </nav>
  </header>
  <main><router-view></router-view></main>
</template>
