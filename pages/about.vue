<template>
  <b-container class="container mw-100 (max-width: 100%;)">
    <b-jumbotron header="About" lead="A little about myself" >
    </b-jumbotron>
  </b-container>
</template>

<script>
// for SEO purposes we can add a function head() to add in data pertaining to each specific page rather than default to the standard info
export default {
  head(){
    return {
      title: 'About',
      meta: [
        { name: 'description', content: 'About description of skills and experience'},
        { name: 'keywords', content: 'about valeshan, valeshan info'},
      ]
    }
  }
}
</script>

<style>

</style>
