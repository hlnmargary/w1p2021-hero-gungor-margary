<template>
  <div class="winMain main">
    <div class="winContent">
    <h1 class="winTitle">{{ message }}</h1>
    <p class="winMessage">{{winMessage}}</p>
    <div class="toiletsContainer">    
      <svg class="toilets" aria-hidden="true"><use xlink:href="#toilets"></use></svg>
    </div>
    <div class="btnWinRestartContainer">
      <div class="btnWinRestart" v-on:click="switchToChar()" >REJOUER</div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      message: 'VICTOIRE', 
      winMessage: 'Mes félicitations cher compatriote, tu peux à présent te soulager la vessie à ton aise.'
    }
  },
  methods: {
    switchToChar() {
      this.$router.push({path: '/characters'})
    }
  }
};
</script>