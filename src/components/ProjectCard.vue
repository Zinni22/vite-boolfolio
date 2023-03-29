<script>
import axios from 'axios';

export default {
name: 'ProjectCard',

  data () {
      return{
        projects: []
      }
  },
  created(){
    axios
    .get('http://127.0.0.1:8000/api/project')
    .then(response => {
        console.log(response.data.projects);

        this.projects = response.data.projects;

    })
  },

  components:{},
  methods:{},

}
</script>

<template>

    <div v-for="project in projects" class="project">
        <h3>
            {{ project.title }}
        </h3>

        <p>
            {{ project.description }}
        </p>

        <span><strong>Link: </strong></span>
        <a href="#">
            {{ project.link }}
        </a>
    </div>
 
</template>

<style lang="scss" scoped>

.project{
    background-color: rgb(253, 225, 230);
    padding: 20px;
    width: calc(100%/4 - 20px);
    margin-bottom: 50px;
    border-radius: 20px;
    cursor: pointer;

    h3{
        margin-bottom: 15px;
    }
    
    p{
        margin-bottom: 15px;
    }
}

</style>
