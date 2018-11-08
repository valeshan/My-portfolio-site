<template>
  <b-container class="container mw-100 (max-width: 100%;) text-center">
    <b-jumbotron header="My portfolio site" lead="A showcase of my projects and skills" >
      <p>For more information visit website</p>
    </b-jumbotron>
    <div class="summary-section">
      <p> Brief list of what kind of projects I can do </p>
    </div>
    <div class="projects-section">
      <p>Insert a project summary here</p>
      <b-button>I am a Button</b-button>
    </div>
  </b-container>
</template>

<script>
import Logo from '~/components/Logo.vue';

export default {
  components: {
    Logo
  }
}
</script>

<style>

  .header-section{
    background-color: rgb(204, 140, 140);
  }
  .summary-section{
    background-color: rgb(204, 204, 204)
  }
  .projects-section{
    background-color: rgb(150, 205, 140);
  }
</style>
