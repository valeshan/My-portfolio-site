<template>
  <!-- <header class="sticky-top home-nav">
    <b-nav>
      <b-nav-item><nuxt-link to="/"><img style="height: 50px; margin: -20px -20px -15px -20px;" :src="menuLogo" alt="logo" /></nuxt-link></b-nav-item>
    </b-nav>
    <b-nav style="justify-self: center" >
      <b-nav-item><nuxt-link to="portfolio">Portfolio</nuxt-link></b-nav-item>
      <b-nav-item><nuxt-link to="about">About</nuxt-link></b-nav-item>
      <b-nav-item><nuxt-link to="contact">Contact</nuxt-link></b-nav-item>
    </b-nav>
  </header> -->

    <!-- <header class="sticky-top navbar-nav" style="margin-left: auto; margin-right: auto;"> -->
  <b-navbar toggleable="md" type="dark" style="width:100wh; height: 4em;" class="home-nav">

    <b-navbar-toggle target="nav_collapse" style="margin-left: 2em;"></b-navbar-toggle>

    <b-navbar-brand href="#" class="mr-auto"><b-nav-item><nuxt-link to="/"><img class="logo" :src="menuLogo" alt="logo" /></nuxt-link></b-nav-item></b-navbar-brand>

      <b-collapse is-nav id="nav_collapse">

        <!-- Right aligned nav items -->
        <b-navbar-nav class="mx-auto" style="justify-self: center">
          <b-nav-item><nuxt-link to="portfolio">Portfolio</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="about">About</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="contact">Contact</nuxt-link></b-nav-item>
        </b-navbar-nav>

      </b-collapse>
  </b-navbar>
  <!-- </header> -->
</template>

<script>
import menuLogo from '@/static/images/menulogo.png';


export default {
  data(){
    return{
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
  }

  .home-nav{
    padding-right: 7em
  }

  li a {
    padding: 1em 2em;
    display: block;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: bold;
    color: white;
    font-size: 0.9em;
  }

  a:hover{
    text-decoration: none;
  }
  li a{
    padding: 1em 2em;
    display: inline-block;    
  }

  #nav_collapse{
    background-image: linear-gradient(to right, #0099ff, #66ffcc);
  }
</style>
