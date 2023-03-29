<script>
import ProjectCard from './ProjectCard.vue';

export default {
name: 'MainApp',

  data () {
      return{
      }
  },

  components:{
    ProjectCard,
  },

  methods:{},

}
</script>

<template>

    <main>
        <h1>Boolfolio</h1>

        <div class="container">
            <ProjectCard />
        </div>

    </main>
 
</template>

<style lang="scss" scoped>

main{
    padding: 50px;
    text-align: center;

    h1{
        margin-bottom: 50px;
    }

    .container{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    
}
</style>
