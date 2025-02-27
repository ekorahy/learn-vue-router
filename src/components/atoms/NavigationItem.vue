<script setup>
defineProps(['name', 'id', 'slug'])
</script>

<template>
  <router-link :to="{ name: 'destination.show', params: { id: id, slug: slug } }">{{
    name
  }}</router-link>
</template>
