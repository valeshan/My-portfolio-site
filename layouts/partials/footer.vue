<template>
  <section class="footer sticky-bottom">
    <span> Valeshan's Portfolio Site 2018</span>
    <span> Email: valeshan@gmail.com </span>
  </section>
</template>

<script>
export default {

}
</script>

<style>
  .footer{
    padding: 1em;
    height: 4em;
    display: grid;
    grid-template-columns: repeat(2,auto);
    background-image: linear-gradient(to right, #0099ff, #66ffcc);;
    width: 100%;
    left: 0px;
  }

  span{
    padding: 1em 2em;
    display: inline;
    text-transform: uppercase;
    font-weight: bold;
    color: white;
    font-size: 0.9em;
  }

  @media screen and (max-width: 500px) {
    .footer{
      height: auto;
      padding: auto;
    }
  }
</style>
