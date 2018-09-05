<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Welcome to my new Scoreboard project, made with Vue.js.<br>
      if you want to learn more about Vue<br>
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <div class="teams">
      <ScoreCounter />
      <ScoreCounter />
    </div>
  </div>
</template>

<script>
import ScoreCounter from './ScoreCounter.vue'

export default {
  name: 'Scoreboard',
  components: {
    ScoreCounter
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
a {
  color: #42b983;
}

.teams {
  display: flex;
  justify-content: space-around;
}
</style>
