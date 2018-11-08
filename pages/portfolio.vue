<template>
  <section >
    <b-container class="container project-container mw-100 (max-width: 100%;)">
      <b-jumbotron class="jumbo-header" header="Portfolio" lead="A few of my projects - 2018" >
      </b-jumbotron>
    </b-container>
    <div class="row">
      <div class="card col-md-5 mx-auto project" style="width: 18rem;" v-bind:key="index" v-for="(project, index) in projectInfo">
          <img v-if="project.image" class="card-img-top" style="height: 20em" :src="project.image" alt="Card image cap">
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
        projectInfo
    }
  },
}
</script>

<style>

.project{
  margin: 1em;
  padding-left: 0;
  padding-right: 0;
}

.jumbo-header{
  background-color:white;
  color: rgb(0,219,146);
  text-align: center;
}

.card-title{
  font-weight: bold;
}

img{
  size: 250px;
}
</style>
