<template>
  <div>
    <client-only>
      <table>
        <tr>
          <th class="score-points">Points</th>
          <th class="score-asteroids">#Asteroids</th>
          <th class="score-date">Date</th>
        </tr>
          <tr v-for="score in leaderboard">
            <td class="score-points">{{ score.points }}</td>
            <td class="score-asteroids">{{ score.destroyedAsteroids }}</td>
            <td class="score-date">{{ formatDate(score.date) }}</td>
          </tr>
      </table>
    </client-only>
  </div>
</template>

<script setup>
  const {
    data: leaderboard,
  } = await $get("/leaderboard");

  const formatDate = (dateString) => {
    const date = new Date(dateString);
    return date.toLocaleString();
  }
</script>

<style scoped>
table {
  width: 100%;
}

tr {
  text-align: center;
}

.score-points {
  text-align: left; 
}
</style>
