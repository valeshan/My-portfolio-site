<template>
    <section class="hero-image">
      <b-container class="mw-100 (max-width: 100%;)">
        <b-jumbotron class="jumbo-header" header="Contact Me" >
        </b-jumbotron>
      </b-container>
      <hr align="center">
      <div class="contact-container container">
        <p>Please feel free to contact me about any queries or projects.</p>
        <p>Email: valeshan@gmail.com</p>
        <p>Mobile: 0449 563 718</p>
      </div>
    </section>
</template>

<script>
export default {
  head(){
    return {
      title: 'Contact',
      meta: [
        { name: 'description', content: 'Contact information'},
        { name: 'keywords', content: 'contact details valeshan, phone email'},
      ]
    }
  }
}
</script>

<style>

.contact-container{
  text-align: center;
  margin-top: 1em;
  margin-bottom: 10em;
}

</style>
