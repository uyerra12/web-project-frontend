<template>
    <div class="card">
        <h3>Name: {{ repo.name }}</h3>
        <h3>Description: {{ repo.description }}</h3>
        <h3>Repo URL: <a :href="repo.repo_url" target="_blank">{{ repo.repo_url }}</a></h3>
        <h3>Date Created: {{ repo.created_at }}</h3>
        <h3>Stargazers Count: {{ repo.stargazers_count }}</h3>
        <h3>has Issues: {{ repo.has_issues }}</h3>
    </div>
</template>

<script>
export default{
    name: 'SingleRepo',
    props:{
        repo: Array
    }
}
</script>

<style>
    .card{
        background-color: rgb(245, 245, 245);
        padding: 10px;
        margin: 10px;
        border: solid 2px rgb(204, 230, 190);
        color: rgb(6, 6, 65);
    }
</style>