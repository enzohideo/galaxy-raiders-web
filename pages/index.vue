<template>
  <div class="menu">
    <h2>Galaxy Raiders</h2>
    <div class="button-wrapper">
      <NuxtLink class="button" to="/game">Start</NuxtLink>
      <NuxtLink class="button" to="/leaderboard">Leaderboard</NuxtLink>
      <NuxtLink class="button" to="/exit">Exit</NuxtLink>
    </div>
  </div>
</template>

<script setup>

</script>

<style>
  :root {
    --button-shadow: 0px 10px 0px #1672b5, 0px 10px 30px #1672b5;
  }

  .menu {
    text-align: center;
    position: absolute;
    top: 45%;
    left: 50%;
    transform: translate(-50%,-50%);
  }

  h2 {
    margin-bottom: 30px;

    font-weight: bold;
    font-size: 75px;

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
    display: block;
    text-align: center;

    position: relative;
    width: 100%;

    color: white;
    background-color: transparent;

    font-weight: bold;
    font-size: 30px;

    margin: 30px auto;
    padding: 25px 40px 25px 40px;
    box-sizing: border-box;

    text-decoration: none;

    border-radius: 30px;
    -webkit-border-radius: 30px;
    -moz-border-radius: 30px;

    box-shadow: var(--button-shadow);
    -webkit-box-shadow: var(--button-shadow);
    -moz-box-shadow: var(--button-shadow);

    transition: all .2s ease;
    -webkit-transition: all .2s ease;
    -moz-transition: all .2s ease;
    -ms-transition: all .2s ease;
    -o-transition: all .2s ease;
  }

  .button:active {
    position: relative;
    transform: translateY(5px);
    box-shadow: unset;
  }

  .button-wrapper {
    display: inline-block;
  }

  @keyframes color-change {
    0%    { color: blue   ; }
    10%   { color: gray   ; }
    20%   { color: white  ; }
    30%   { color: yellow ; }
    40%   { color: orange ; }
    50%   { color: pink   ; }
    60%   { color: orange ; }
    70%   { color: yellow ; }
    80%   { color: white  ; }
    90%   { color: gray   ; }
    100%  { color: silver ; }
  }
</style>
