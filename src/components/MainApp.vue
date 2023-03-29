<script>
import axios from 'axios';

export default {
name: 'MainApp',

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

    <main>
        <h1>Boolfolio</h1>
    </main>
 
</template>

<style lang="scss" scoped>

</style>
