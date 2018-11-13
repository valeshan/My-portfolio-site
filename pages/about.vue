<template>
  <section class="wallpaper about-page"> 
    <b-jumbotron class="about-jumbo text-center">
        <div class="jumbo-content">
          <img :src="logoImage" alt="logo" style="height: 10em" />
          <div style="color: white; padding-top: 7em; margin-bottom: -7em">
            <h3>About Me</h3>
          </div>
        </div>
      </b-jumbotron> 
    <div class="container">
      <br>
      <!-- <img class="circle center" :src="image" alt="face"> -->
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
      <hr class="center" style="border-color:white;">
      <div class="row">
        <div class="col-md-8 paragraphs">
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

import logoImage from '@/static/images/logov3.png';

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
      logoImage
    }
  }
}
</script>

<style>
  .about-page{
    display: grid;
  }

  .about-jumbo{
    background-image: url('../static/images/aboutCover.jpg');
    background-repeat:no-repeat;
    background-size: cover;
    background-position: bottom;
    background-attachment: fixed;
    position: relative;
    padding: 13em;
    margin-bottom: -1em;
  }

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

  .paragraphs{
    margin-right: auto;
    margin-left: auto;
  }

  @media screen and (max-width: 500px) {
    .paragraphs{
      width: 24em;
      text-align: left;
      margin-right: auto;
      margin-left: 1em;
      font-size: 15px;
    }

    .link-group{
      margin-left: -8em;
    }
    hr{
      display: none;
    }
    .center{
      margin-left: 8em;
    }

    .about-jumbo{
      margin-left: -5em;
    }
  }

  @media screen and (min-width: 501px) and(max-width: 1000px) {
    .paragraphs{
      width: 24em;
      text-align: left;
      margin-right: auto;
      margin-left: auto;
      font-size: 15px;
    }

    .link-group{
      margin-left: -11em;
    }

    hr{
      display: none;
    }

    .center{
      margin-left: 8em;
    }
  }

</style>
