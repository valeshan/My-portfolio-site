<template>
  <!-- <b-container class="container mw-100 (max-width: 100%;)">
    <b-jumbotron header="Projects" lead="Previous projects" >
      <p>For more information visit website</p>
    </b-jumbotron>
    <div>
      <b-card no-body>
        <b-nav pills slot="header" v-b-scrollspy:nav-scroller>
            <b-nav-item v-bind:key="index" v-for="(project, index) in projectInfo" :href="'#' + index" @click="scrollIntoView">{{project.name}}</b-nav-item>
        </b-nav>
        <b-card-body id="nav-scroller"
            ref="content"
            style="position:relative; height: 50em; overflow-y:scroll;">
            <div class= "pop" v-bind:key="index" v-for="(project, index) in projectInfo"> 
              <h3 :id="index" style="margin-bottom: 1em" v-text="project.name"></h3>
              <img class="w-75" :src="project.image" />
              <p> {{project.text}} </p>
            </div>
        </b-card-body>
      </b-card>
  </div>
  </b-container> -->
  <section >
    <div class="row mx-auto">
      <div class="card col-md-5 mr-auto project" style="width: 18rem;" v-bind:key="index" v-for="(project, index) in projectInfo">
          <img class="card-img-top" style="height: 20em" :src="project.image" alt="Card image cap">
          <div class="card-body">
            <h5 class="card-title">{{project.name}}</h5>
            <p class="card-text">{{project.text}}</p>
            <a v-if="project.href"  :href="project.href" class="btn outline-primary" target="_blank">Live site</a>
            <a v-if="project.github"  :href="project.github" class="btn outline-danger" target="_blank">Repo</a>
            <div class="collapse" id="collapseExample">
              <div class="card card-body">
                {{project.text}}
              </div>
            </div>
          </div>
      </div>
    </div>
  </section>
</template>

<script>
import projectInfo from '@/static/projectInfo.js';

export default {
  head(){
    return {
      title: 'Projects',
      meta: [
        { name: 'description', content: 'List of repos and project links'},
        { name: 'keywords', content: 'project information and repo links'},
      ]
    }
  },
  data() {
    return {
        sampleText: `
          Quis magna Lorem anim amet ipsum do mollit sit cillum voluptate ex nulla
          tempor. Laborum consequat non elit enim exercitation cillum aliqua
          consequat id aliqua. Esse ex consectetur mollit voluptate est in duis
          laboris ad sit ipsum anim Lorem. Incididunt veniam velit elit elit veniam
          Lorem aliqua quis ullamco deserunt sit enim elit aliqua esse irure. Laborum
          nisi sit est tempor laborum mollit labore officia laborum excepteur
          commodo non commodo dolor excepteur commodo. Ipsum fugiat ex est consectetur
          ipsum commodo tempor sunt in proident.`,
        projectInfo
    }
  },
}
</script>

<style>

/* button a{
    display: block;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 0.9em;
} */

li a{
  color: black;
}

.project{
  margin: 1em;
  padding-left: 0;
  padding-right: 0;
}

.card-title{
  font-weight: bold;
}

img{
  size: 250px;
}
</style>
