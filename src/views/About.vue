<template>
  <div class="container">
    <p>
      Après avoir appris {{vuejs}}, j'ai décidé de faire ce petit projet
       un peu cool si vous trouvez &#128521; . il n'y aura pas trop de mise à 
       jour car ce n'est pas un projet à long terme, je voulais juste m'amuser.
       <br>
       j'ai utilisé l'API Gnews pour récupérer les données, 
       alors je vous donne les liens en bas, amusez-vous aussi &#128515;.
    </p>
    <br>
    <p>
      <a href="https://gnews.io/">Gnews API (google news data)</a>
      <br>
      <a href="https://netlify.com/">Netlify (hosting)</a>
    </p>
  </div>
</template>

<script>
  export default {
    data() {
      return{
        vuejs: "{{ Vuejs }}"
      }
    }
  }
</script>

<style scoped>
  p{
    font-size: 30px;
  }
</style>
