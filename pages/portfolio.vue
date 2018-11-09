<template>
  <section class="hero-image">
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
            <ul class="row tools">
              <li class="col-md-3 tool" :key="index" v-for="(tool, index) in project.tools">{{tool}}</li>
            </ul>
            <br>
            <a v-if="project.href"  :href="project.href" class="btn link-btn" target="_blank">Live site</a>
            <a v-if="project.github"  :href="project.github" class="btn link-btn" target="_blank">Repo</a>
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

ul{
  list-style: none;
}

.tools{
  margin-left: -2.5em;
}

.tool{
  text-decoration: none;
  text-align: center;
  color: rgb(0, 139, 219);
  background-color: white;
  border: solid white;
  padding: 3px;
  margin-right: 5px;
  margin-bottom: 5px;
}

.link-btn{
  color: white;
  border: solid white;
  margin-top: -1em;
}

.link-btn:hover{
  color: white;
  border: solid rgb(0,219,146);
}

.card-title{
  font-weight: bold;
  color:white;
}

.card-text{
  color: white;
  font-weight: 500;
}

.card-body{
  background-color: rgb(0, 168, 219);
}

img{
  size: 250px;
}
</style>
