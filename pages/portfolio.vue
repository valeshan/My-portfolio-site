<template>
  <section class="wallpaper">
    <b-container class="container project-container mw-100 (max-width: 100%;)">
      <b-jumbotron class="jumbo-header" header="Portfolio" lead="A few of my projects - 2018" >
      </b-jumbotron>
    </b-container>
    
    <div class="row">
      <div class="col-md-5 mx-auto project box" style="width: 18rem;" v-bind:key="index" v-for="(project, index) in projectInfo">
          <img v-if="project.image" class="card-img-top box" style="height: 19em" :src="project.image" alt="Card image cap">
          <div class="card-body" v-scroll="handleScroll">
            <h5 class="card-title">{{project.name}}</h5>
            <p class="card-text">{{project.text}}</p>
            <a v-b-toggle.toolcollapse class="btn link-btn" style="color: white">Tools</a>

            <b-collapse id="toolcollapse"> 
              <ul class="row tools">
                <li class="col-md-3 tool" :key="index" v-for="(tool, index) in project.tools">{{tool}}</li>
              </ul>
            </b-collapse>
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
  methods: {
  }
}
</script>

<style>

.project{
  margin: 1em;
  padding-left: 0;
  padding-right: 0;
  background-color: linear-gradient(to right, #6fa9df 0%, #7fe9f7 100%);
}

ul{
  list-style: none;
}

.tools{
  margin-top: 20px;
  margin-left: -2.5em;
}

.tool{
  text-decoration: none;
  text-align: center;
  color: #27b188;
  background-color: white;
  border: solid white;
  padding: 3px;
  margin-right: 5px;
  margin-bottom: 5px;
}

.link-btn{
  color: white;
  border: solid white;
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
  width: 613.5px;
  margin-top: 0.5em;
  background-image: linear-gradient(to right, #17c59a 0%, #2fd4da 100%);
  background-position: bottom right;
}

#toolcollapse{
  margin-top: 10px;
}

img{
  size: 250px;
}

@media screen and (max-width: 500px) {

  .project{
    padding: 0;
  }

  .card-text{
    font-size: 15px;
  }

  .card-body, .card-img-top{
    width: 22em;
    margin-left: -33px;
  }

  .link-btn{
    margin-top: -2em;
    margin-bottom: -2em;
  }
}

@media screen and (min-width: 501px){
  .card-body{
    width: auto;
  }
}
</style>
