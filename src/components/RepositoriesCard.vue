<template>
    <div v-for="repo of repos" :key="repo.id" >

        <SingleRepo :repo=repo />

    </div>
</template>

<script>
import SingleRepo from './SingleRepo.vue'

    export default{
        name: 'RepositoriesCard',
        components:{
            SingleRepo
        },
        props:{
            repos: Array
        }
    }
</script>

<style>
    
</style>