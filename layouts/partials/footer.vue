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
    background: rgb(0,219,146);
    padding: 1em;
    display: grid;
    grid-template-columns: repeat(2,auto);
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
</style>
