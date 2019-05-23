<template>
  <div class="homeMain main">
    <div class="loaderContainer">    
      <svg class="loader" aria-hidden="true"><use xlink:href="#loader"></use></svg>
    </div>
    <div class="homeContent">
      <h1>{{ message }}</h1>
      <router-link class="button" to="/characters">Jouer</router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "INTRO + RÈGLES DU JEU"
    };
  },
  methods: {
    onOpen() {
	    setInterval(function(){
        alert("Hello world"); 
      }, 3000);
    }
  }
};
</script>
