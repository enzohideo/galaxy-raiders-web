<template>
  <div>

    <h2> GALAXY &nbsp;RAIDERS </h2>

    <ul>
      <li><NuxtLink class="button" to="/game">Start</NuxtLink></li>
      <li><NuxtLink class="button" to="/leaderboard">Leaderboard</NuxtLink></li>
      <li><NuxtLink class="button" to="/exit">Exit</NuxtLink></li>
    </ul>

  </div>
</template>

<script setup>

</script>

<style>
  body {
     background-image: url('/assets/space.png');
  }
  h2 {
    font-family: serif; 
    color: white;
    margin-bottom: 30px;
    font-size: 75px;
    text-align: center;
    font-weight: bold;
    position: absolute;
    top: 10%;
    width: 100%;
    animation: color-change 4s infinite;
    text-shadow: 
    0 1px 0 hsl(174,5%,80%),
    0 2px 0 hsl(174,5%,75%),
    0 3px 0 hsl(174,5%,70%),
    0 4px 0 hsl(174,5%,66%),
    0 5px 0 hsl(174,5%,64%),
    0 6px 0 hsl(174,5%,62%),
    0 7px 0 hsl(174,5%,61%),
    0 8px 0 hsl(174,5%,60%),
    0 0 5px rgba(0,0,0,.05),
    0 1px 3px rgba(0,0,0,.2),
    0 3px 5px rgba(0,0,0,.2),
    0 5px 10px rgba(0,0,0,.2),
    0 10px 10px rgba(0,0,0,.2),
    0 20px 20px rgba(0,0,0,.3);
  }

  .button {
    position: relative;
    top: 140px;
    color: white;
    width: 300px;
    text-decoration: none;
    background-color: none;
    font-weight: bold;
    font-size: 40px;
    display: block;
    padding: 10px;
    border-radius: 10px;
    -webkit-border-radius: 30px;
    -moz-border-radius: 10px;
    box-shadow: 0px 10px 0px #1672b5, 0px 10px 30px #1672b5;
    -webkit-box-shadow: 0px 10px 0px #1672b5, 0px 10px 30px #1672b5;
    -moz-box-shadow: 0px 10px 0px #1672b5, 0px 10px 30px #1672b5;
    margin: 30px auto;
    text-align: center;
    transition: all .2s ease;
    -webkit-transition: all .2s ease;
    -moz-transition: all .2s ease;
    -ms-transition: all .2s ease;
    -o-transition: all .2s ease;
  }

  .button:active {
    position: relative;
    top: 145px;
    -webkit-box-shadow: 0px 3px 0px #095e9c, 0px 9px 25px #095e9c;
    -moz-box-shadow: 0px 3px 0px #095e9c, 0px 9px 25px #095e9c;
    box-shadow: 0px 3px 0px #095e9c, 0px 9px 25px #095e9c;
  }

  @keyframes color-change {
    0% { color: light-blue; }
    10% { color: gray; }
    20% { color: white; }
    30% { color: yellow; }
    40% { color: orange; }
    50% { color: pink; }
    60% { color: orange; }
    70% { color: yellow; }
    80% { color: white; }
    90% { color: gray; }
    100% { color: silver; }
  }
</style>
