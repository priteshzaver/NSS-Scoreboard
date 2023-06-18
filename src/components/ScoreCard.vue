<script setup>
const props = defineProps(['team'])
const emit = defineEmits(['minus', 'plus'])
</script>

<template>
  <div>
    {{ props.team.score }}
  </div>
  <div>
    <button @click="emit('minus')">minus</button>
    <button @click="emit('plus')">plus</button>
  </div>
</template>

<style scoped></style>
