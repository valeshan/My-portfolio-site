<template>
  <header class="sticky-top">
    <b-nav>
      <b-nav-item><nuxt-link to="/">My Portfolio</nuxt-link></b-nav-item>
    </b-nav>
    <b-nav style="justify-self: right">
      <b-nav-item><nuxt-link to="/">Home</nuxt-link></b-nav-item>
      <b-nav-item><nuxt-link to="portfolio">Portfolio</nuxt-link></b-nav-item>
      <b-nav-item><nuxt-link to="about">About</nuxt-link></b-nav-item>
      <b-nav-item><nuxt-link to="contact">Contact</nuxt-link></b-nav-item>
    </b-nav>
  </header>
</template>

<script>
export default {

}

</script>

<style>
  header{
    background: rgb(0,219,146);
    display: grid;
    grid-template-columns: repeat(2,auto);
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
</style>
