<template>
  <section> 
    <b-container class="about-container mw-100 (max-width: 100%;)">
      <b-jumbotron class="jumbo-header" header="Valeshan Naidoo" lead="A little about myself and experiences" >
      </b-jumbotron>
    </b-container>
    <div class="container">
      <hr class="center">
      <img class="circle center" :src="image" alt="face">
      <hr class="center">
      <div class="row">
        <div class="col-md-8  mx-auto">
          <p v-bind:key="index" v-for="(paragraph, index) in aboutInfo">
            {{paragraph}}
          </p>          
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// for SEO purposes we can add a function head() to add in data pertaining to each specific page rather than default to the standard info
import aboutInfo from '@/static/aboutInfo.js';
export default {
  head(){
    return {
      title: 'About',
      meta: [
        { name: 'description', content: 'About description of skills and experience'},
        { name: 'keywords', content: 'about valeshan, valeshan info'},
      ]
    }
  },
  data(){
    return{
      aboutInfo,
      image: 'https://i.imgur.com/9Ng05r1.jpg',
    }
  }
}
</script>

<style>

  .about-container{
    text-align: center;
    margin-top: 1em;
    margin-bottom: auto;
  }

  .circle {
  border-radius: 50%;
  width: 130px;
  height: 130px; 
  }


</style>
