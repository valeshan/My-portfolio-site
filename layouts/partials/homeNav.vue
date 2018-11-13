<template>
  <b-navbar toggleable="md" type="dark" style="width:100wh;" class="home-nav">

    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

    <b-navbar-brand href="#" ><b-nav-item><nuxt-link to="/"><img class="logo" :src="menuLogo" alt="logo" /></nuxt-link></b-nav-item></b-navbar-brand>

      <b-collapse is-nav id="nav_collapse" style="background: none;">

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

  .home-nav{
    padding-right: 7em
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
    text-decoration: none;
  }

  #nav_collapse{
    background-image: linear-gradient(to right, #0099ff, #66ffcc);
  }

  @media screen and (min-width: 500px) {
    .home-nav{
      height: 4em;
    }
  }
</style>
