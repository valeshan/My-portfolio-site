<template>
    <section class="wallpaper">
      <b-container class=" contact-container mw-100 (max-width: 100%;)">
        <b-jumbotron class="contact-header" header="Contact Me">
        </b-jumbotron>
      </b-container>
      <div class="contact-content container">
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
  margin-top: 5em;
}

.contact-header{
  background: none;
  text-align: center;
}

.contact-content{
  text-align: center;
  margin-top: 4em;
  margin-bottom: 10em;
}

@media screen and (max-width: 500px) {
  .contact-content{
      width: 24em;
      text-align: left;
      margin-right: auto;
      margin-left: 1em;
      font-size: 15px;
  }
  .contact-header{
    text-align: justify;
  }

}

</style>
