<template>
<div>
  <b-container>
    <div class="row">
      <div class="col-lg-3 col-md-4 col-sm-6 col-xs-1 mb-3" v-for="article in articles" :key="article">
        <b-card
        no-body
    style="max-width: 20rem;"
    :img-src="articles.image"
    img-alt="Image"
    img-top
    v-if="article"
    >
            <template v-slot:header>
              <h4 class="mb-0">{{article.title}}</h4>
            </template>

            <b-card-body>
              <b-card-text>
                {{article.description}}
              </b-card-text>
            </b-card-body>

            <template v-slot:footer>
                <small class="text-muted">{{article.date}}</small>
            </template>
        </b-card>
      </div>
    </div>
    <div v-if="printError" class="alert alert-danger container" role="alert">
              {{printError}}
    </div>
  </b-container>
</div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'HelloWorld',

  data(){
    return{
      articles: {
        title: '',
        description: '',
        date: '',
        image: ''
      },
      printError: "",
    }
  },

  mounted(){
    const apiKey = "d7216f8e81747dbef16cabf1b9ce825d";

    axios.get(`https://gnews.io/api/v3/search?q=technology&token=${apiKey}`)
      .then(response => {
        this.articles = response.data.articles;
        this.articles.title = response.data.articles.title;
        this.articles.description = response.data.articles.description;
        this.articles.date = response.data.articles.publishedAt;
        this.articles.image = response.data.articles.image;
        console.log(response.data.articles);
      })
      .catch(error => {
        console.log(error);
        error = "Impossible d'afficher les articles, Nombres de requêtes atteintes";
        this.printError = error;
      })
  }
}
</script>

<style scoped>

</style>
