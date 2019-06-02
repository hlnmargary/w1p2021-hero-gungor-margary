<template>
  <div class="homeMain main">
    <div class="loaderContainer">    
      <svg class="loader" aria-hidden="true"><use xlink:href="#loader"></use></svg>
    </div>
    <div class="homeContent">
      <h1 class="introTitle">{{ introTitle }}</h1>
      <div class="introContainer">
        <p class="introContent">{{ introContent }}</p>
      </div>
      <h1 class="goalTitle">{{ goalTitle }}</h1>
      <div class="goalContainer">
        <p class="goalContent">{{ goalContent }}</p>
      </div>
      <h1 class="rulesTitle">{{ rulesTitle }}</h1>
      <div class="rulesContainer"> 
        <p class="rulesContent">{{ rulesContent }}</p>
      </div>
      <div class="btnHomeContainer">
        <div class="btnHome" v-on:click="switchToChar()">JOUER</div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      introTitle: "Introduction",
      goalTitle: "Objectif",
      rulesTitle : "Règles",
      introContent: "Mince, tu as une envie très pressante, ça tombe mal : ton appartement est à l'autre bout de la ville",
      goalContent: "Fais les bons choix afin d'arriver sans encombre à la victoire. Attention, tous les chemins mènent à Rome, mais pas aux toilettes !",
      rulesContent : "À coup de clicks, le chemin vers chez toi tu trouveras"
    }
  }, 
  methods: {
    switchToChar() {
      this.$router.push({path: '/characters'})
    }
  }
};
</script>
