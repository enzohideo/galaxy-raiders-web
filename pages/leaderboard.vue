<template>
  <div class="center table-wrapper">
    <client-only>
      <table>
        <thead>
          <th>Points</th>
          <th>#Asteroids</th>
          <th>Date</th>
        </thead>
        <tbody v-for="score in leaderboard">
          <td class="score-points">{{ score.points }}</td>
          <td class="score-asteroids">{{ score.destroyedAsteroids }}</td>
          <td class="score-date">{{ formatDate(score.date) }}</td>
        </tbody>
      </table>
    </client-only>
  </div>
</template>

<script setup>
  const {
    data: leaderboard,
  } = await $get("/leaderboard");

  function formatDate(dateString) {
    const date = new Date(dateString);
    return date.toLocaleString([],{
      hour12: false,
    }).replace(' ', '\u00A0');
  }
</script>

<style scoped>
  .table-wrapper {
    border-radius: 15px;
    border: 3px solid white;
  }

  table {
    border-collapse: collapse;
    text-align: center;
    font-size: 20px;
  }

  th {
    padding: 25px;
  }

  td {
    padding: 10px;
  }

  tbody:hover {
    background-color: rgba(255, 255, 255,0.1);
  }

  thead {
    border-bottom: 3px solid white;
  }

  .score-points {
    text-align: right;
  }
</style>
