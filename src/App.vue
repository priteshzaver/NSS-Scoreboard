<script setup>
import { ref } from 'vue'
import MatchupTitle from './components/MatchupTitle.vue'
import ScoreCard from './components/ScoreCard.vue'
import GameStatus from './components/GameStatus.vue'

const team1 = ref({
  name: 'Team 1',
  score: 0
})
const team2 = ref({
  name: 'Team 2',
  score: 0
})

const minusPoint = (team) => {
  if (team.score > 0) {
    team.score--
  }
}
const addPoint = (team) => {
  team.score++
}
</script>

<template>
  <MatchupTitle :team1="team1" :team2="team2" />
  <GameStatus :team1="team1" :team2="team2" />
  <div>
    <ScoreCard :team="team1" @minus="minusPoint(team1)" @plus="addPoint(team1)" />
    <ScoreCard :team="team2" @minus="minusPoint(team2)" @plus="addPoint(team2)" />
  </div>
</template>

<style scoped></style>
