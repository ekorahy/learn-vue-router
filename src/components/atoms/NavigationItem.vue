<script setup>
defineProps(['name', 'path'])
</script>

<template>
  <router-link :to="path">{{ name }}</router-link>
</template>
