<template>
  <section class="wallpaper home-page">
      <b-jumbotron class="hero-jumbo text-center">
        <img :src="logoImage" alt="logo" style="height: 10em" fluid />
        <div style="color: white; padding-top: 1em;">
          <h3>Valeshan Naidoo</h3>
          <p>Full Stack Developer / Web Developer</p>
        </div>
        <b-nav class="project-button row">
          <b-nav-item class="mx-auto"><nuxt-link class="project-link" to="portfolio">My Portfolio</nuxt-link></b-nav-item>
        </b-nav>
        <b-container>
          <div class="projects-section">
            <p>
              Simple static sites, single page apps (SPAs) and full-stack web apps w/ backend.
            </p>
          </div>
        </b-container>
      </b-jumbotron> 
    <homeNav class="index-nav"/>
    <br>
    <div class="container">
      <div class="summary-section">
        <img class="icon" :key="index" v-for="(image, index) in images" :src="image"/>
      </div>
      <br>
    </div>
  </section>
</template>

<script>
import homeNav from '@/layouts/partials/homeNav';

import reactImage from '@/static/images/react.png';
import cssImage from '@/static/images/css.png';
import htmlImage from '@/static/images/html.png';
import mongodbImage from '@/static/images/mongodb.png';
import sqlImage from '@/static/images/sql.jpg';
import vueImage from '@/static/images/vue.png';
import javascriptImage from '@/static/images/javascript.png';
import nodejsImage from '@/static/images/nodejs.png';

import logoImage from '@/static/images/logov3.png';
import landingBackgroundImage from '@/static/images/landing-background.png';


export default {
  components: {
    homeNav
  },
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
      ],
      logoImage,
      landingBackgroundImage
      }
    }
  }
</script>

<style>

  .home-page{
    display: grid;
  }

  .icon{
    height: 7em;
    width: 7em;
    padding: 1em;
  }

  .projects-section{
    position: absolute;
    color: white;
    margin-top: 6em;
    font-size: 20px;
  }

  .project-link{
    background-color: none;
    color: white;
    border: solid; 
    /* border-radius: 3px; */
    margin-top: 1em;
    border-image: linear-gradient(to right, #6fa9df 0%, #7fe9f7 100%);
    border-image-slice: 1;
  }

  .project-link:hover{
    transition: ease-in 0.3s;
    color: white;
    background-color: rgba(256, 256, 256, 0.2);
  }

  .hero-jumbo{
    background: url('../static/images/landing-background.png') no-repeat center center;
    /* background-repeat:no-repeat; */
    background-size: cover;
    /* background-position: 50% 70%; */
    background-attachment: fixed;
    position: relative;
    padding: 13em;
    margin-bottom: -1em;
  }

  .summary-section{
    margin-left: 7em;
    margin-top: -1em;
    margin-bottom: -4em;
  }

</style>
