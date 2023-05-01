<template>
  <MyHeader name="Ujwala Yerra" />
  <RepositoriesCard :repos= repos />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import RepositoriesCard from './components/RepositoriesCard.vue'

export default{
  name: 'App',
  components:{
    MyHeader,
    RepositoriesCard
  },
  data(){
    return{
      repos: []
    }
  },
  methods:{
    async getRepos(){
      const data = await fetch('http://localhost:5050/api');
      const result = await data.json()
      console.log(result);
      return result;
    }
  },
  async created(){
    this.repos = await this.getRepos();
  }
}
    
   
</script>

<style>

</style>
