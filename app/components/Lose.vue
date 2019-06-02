<template>
  <div class="loseMain main">
    <div class="loseContent">
      <h1 class="loseTitle">{{message}}</h1>
      <h2 class="loseMessage">{{endMessage}}</h2>
      <div class="btnRestartContainer">
        <div class="btnRestart" v-on:click="switchToChar()" >RECOMMENCER</div>
      </div>
    </div>
  </div>
</template>

<script>
import gameService from '../services/gameService';
import game from '../data.json';

export default {
  data() {
    return {
      show: true,
      gameService: gameService,
      message: "GAME OVER",
      endMessage: gameService.endContent
    }
  },
  methods: {
    switchToChar() {
      this.$router.push({path: '/characters'})
    }
  }
};
</script>