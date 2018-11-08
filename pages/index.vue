<template>
  <section>
    <b-container class="container home-container mw-100 (max-width: 100%;) text-center">
      <b-jumbotron class="jumbo-header" header="Developer for hire." lead="Full Stack Developer / Web Developer" >
      </b-jumbotron>
    </b-container>
    <br>
    <div class="container">
      <div class="summary-section">
        <p>
          I can develop simple static sites, single page apps (SPAs) and full-stack web apps w/ backend.
        </p>
        <br>
        <p>
          Here are some of the languages, libraries and frameworks I can work with:
        </p>
        <img class="icon" :key="index" v-for="(image, index) in images" :src="image" />
      </div>
      <br>
      <div class="projects-section">
        <p>You can look at examples of all the above tools in action in my portfolio page!</p>
        <b-nav class="center mx-auto">
          <b-nav-item><nuxt-link class="project-link" to="portfolio">My Portfolio</nuxt-link></b-nav-item>
        </b-nav>
      </div>
    </div>
  </section>
</template>

<script>
import reactImage from '@/static/images/react.png';
import cssImage from '@/static/images/css.png';
import htmlImage from '@/static/images/html.png';
import mongodbImage from '@/static/images/mongodb.png';
import sqlImage from '@/static/images/sql.jpg';
import vueImage from '@/static/images/vue.png';
import javascriptImage from '@/static/images/javascript.png';
import nodejsImage from '@/static/images/nodejs.png';


export default {
  data(){
    return{
      images: [
        cssImage,
        htmlImage,
        mongodbImage,
        sqlImage,
        reactImage,
        vueImage,
        javascriptImage,
        nodejsImage,
      ]
      }
    }
  }
</script>

<style>
  .icon{
    height: 7em;
    width: 7em;
    padding: 1em;
  }
  
  .project-link{
    background-color: blue;
    color: white
  }

  .project-link:hover{
    transition: ease-in 0.3s;
    color: white;
    background-color: rgb(0,219,146);
  }
  /* .header-section{
    background-color: rgb(204, 140, 140);
  }
  .summary-section{
    background-color: rgb(204, 204, 204)
  }
  .projects-section{
    background-color: rgb(150, 205, 140);
  } */


</style>
