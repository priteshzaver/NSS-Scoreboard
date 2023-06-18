<script setup>
const props = defineProps(['team1', 'team2'])
</script>

<template>
  <div>
    <div>
      <div :class="{ winning: props.team1.score > props.team2.score }">
        {{ props.team1.name }}
      </div>
      <div>vs.</div>
      <div :class="{ winning: props.team2.score > props.team1.score }">
        {{ props.team2.name }}
      </div>
    </div>
  </div>
</template>

<style scoped>
.winning {
  color: goldenrod;
}
</style>
