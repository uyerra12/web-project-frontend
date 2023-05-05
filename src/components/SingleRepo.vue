<template>
    <div class="card">
        <div class="child" id="repo_info">
            <h3><span style="color:#a52a2a;">Repository Name: </span> {{ repo.name }}</h3>
            <h3><span style="color:#4682b4;">Description: </span> {{ repo.description }}</h3>
            <h3><span style="color:#228b22;">Repo URL: </span><a :href="repo.repo_url" target="_blank">{{ repo.repo_url }}</a></h3>
            <h3><span style="color:#dc143c;">Date Created: </span>{{ repo.created_at }}</h3>
            <h3><span style="color:#ff0000;">Stargazers Count: </span>{{ repo.stargazers_count }}</h3>
            <h3><span style="color:#ff1493;">has Issues: </span>{{ repo.has_issues }}</h3>
        </div>
        
        <!-- <h3><span style="color: #A833FF;">Languages Used: </span>{{ repo.languages_used }}</h3> -->
        <div class="child" id="pie">
            <LanguagesUsed :languages_used="repo.languages_used" />
        </div>
        
    </div>
</template>

<script>
import LanguagesUsed from './LanguagesUsed.vue';
export default{
    name: "SingleRepo",
    props: {
        repo: Array,
    },
    components: { LanguagesUsed }
}
</script>

<style>
    .card{
        background-color: #f0ffff;
        padding: 10px;
        margin: 10px;
        border: solid 2px rgb(204, 230, 190);
        color: rgb(6, 6, 65);
    }
    .child{
        display: inline-block;
    }
    #repo_info{
        width: 50%;
        padding: 10px;
    }
</style>