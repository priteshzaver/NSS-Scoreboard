<script setup>
const props = defineProps(['team1', 'team2'])
</script>

<template>
  <h1>{{ props.team1.name }} vs. {{ props.team2.name }}</h1>
</template>

<style scoped></style>
