<template>
  <header>
    <b-nav>
      <b-nav-item><nuxt-link to="/"
      class="logo">My Portfolio</nuxt-link></b-nav-item>
    </b-nav>
    <b-nav pills style="justify-self: right">
        <b-nav-item><nuxt-link to="/">Home</nuxt-link></b-nav-item>
        <b-nav-item><nuxt-link to="projects">Projects</nuxt-link></b-nav-item>
        <b-nav-item><nuxt-link to="contact">Contact</nuxt-link></b-nav-item>
        <b-nav-item><nuxt-link to="about">About</nuxt-link></b-nav-item>
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

  .logo, li a {
    padding: 1em 2em;
    display: block;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: bold;
    color: white;
    font-size: 0.9em;
  }

  li a{
    padding: 1em 2em;
    display: inline-block;    
  }
</style>
