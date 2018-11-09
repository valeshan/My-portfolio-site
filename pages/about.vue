<template>
  <section class="hero-image"> 
    <b-container class="about-container mw-100 (max-width: 100%;)">
      <b-jumbotron class="jumbo-header" header="Valeshan Naidoo" lead="A little about myself and experiences" >
      </b-jumbotron>
    </b-container>
    <div class="container">
      <hr class="center">
      <img class="circle center" :src="image" alt="face">
      <div class="row link-group">
        <div class="mx-auto">
          <a :href="linkedin" target="_blank" class="profile-link">
            <img :src="linkedinImage" alt="linkedin" style="width: 2em;" />   
          </a>
          <a :href="github" target="_blank">
          <img :src="githubImage" alt="github" style="width: 2em;" />   
          </a>  
        </div>
      </div>
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
import linkedinImage from '@/static/images/linkedin.png';
import githubImage from '@/static/images/github.png';

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
      linkedin: 'http://linkedin.com/in/valeshan-naidoo-4ab63553/',
      github: 'http://github.com/valeshan',
      linkedinImage,
      githubImage,
    }
  }
}
</script>

<style>
  .link-group{
    margin-top: 1.5em;
  }

  .profile-link{
    margin-right: 1em;
  }

  .about-container{
    text-align: center;
    margin-top: 1em;
  }

  .jumbo-header{
    background: none;
  }

  .circle {
  border-radius: 50%;
  width: 130px;
  height: 130px; 
  }


</style>
