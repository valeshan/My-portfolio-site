<template>
  <header class="sticky-top navbar-nav">
  <b-navbar toggleable="md" type="dark" style="width:100wh">

    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

    <b-navbar-brand href="#"><b-nav-item><nuxt-link to="/"><img class="logo" :src="menuLogo" alt="logo" /></nuxt-link></b-nav-item></b-navbar-brand>

      <b-collapse is-nav id="nav_collapse" >

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item><nuxt-link to="/">Home</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="portfolio">Portfolio</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="about">About</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="contact">Contact</nuxt-link></b-nav-item>

        </b-navbar-nav>

      </b-collapse>
  </b-navbar>
  </header>

</template>

<script>
import logoImage from '@/static/images/logov2.png';
import logoImage2 from '@/static/images/logoprint.png';
import menuLogo from '@/static/images/menulogo.png';


export default {
  data(){
    return{
      logoImage,
      logoImage2,
      menuLogo,
    }
  }
}

</script>

<style>
  header{
    background: rgb(0,219,146);
    display: grid;
    grid-template-columns: repeat(2,auto);
    height: 4em;
  }


  li{     
    list-style: none;
  }

  li a {
    padding: 1em 2em;
    display: inline-block; 
    text-transform: uppercase;
    text-decoration: none;
    font-weight: bold;
    color: white;
    font-size: 0.9em;
  }

  a:hover{
    text-decoration: underline;
    color: white;
  }

</style>
