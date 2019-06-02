<template>
  <div class="enigmaMain main">
    <h1 class="enigmaTitle">Enigme</h1>
    <ul class="enigmaList">
      <li class="enigmaItem">Mon premier est le nombre de saison de Game of Thrones</li>
      <li class="enigmaItem">Mon deuxième est la quatrième lettre du nom du bar préféré des Héticiens</li>
      <li class="enigmaItem">Mon troisième est le meilleur groupe de la promo</li>
      <li class="enigmaItem">Mon quatrième est le nombre de films dans lequel a joué Bastien Calou</li>
      <li class="enigmaItem">Mon cinquième est le nombre de lettres dans Amsellem, moins le nombre de lettres dans Yves</li>
    </ul>
    <form action="" method="get" class="form-example">
      <div class="formInput">
        <label for="char1"> </label>
        <input v-on:keyup="doEnigma()" class="input" type="text" name="char1" id="char1" maxlength="5" required >
      </div>
    </form>
  </div>
</template>

<script>
import game from "../data.json";

export default {
  methods: {
    doEnigma() {
      var input = document.querySelector('.formInput input[name=char1]');
      var value = ""; 

      value += input.value;
      
      if (value === '8D214') {
        this.$router.push({path: '/win'})
      } 
      if (value.length === 5 && input.value !== '8D214') {
        this.$router.push({path: '/lose'})
      }
    }
  }
}
</script>