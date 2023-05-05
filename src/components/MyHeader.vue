<template>
    <div>
        <h2 style="text-align: left; color: #00008b;">Name: {{ name }}</h2>
        <h2 style="text-align: left; color: #00008b;">Student ID: 00763341</h2>
        <h2 style="text-align: left; color: #00008b;">Project: Github Repositories</h2>
    </div>
    
</template>

<script>
    export default{
        name: 'MyHeader',
        props:{
            name: String
        }
    }
</script>

<style>
</style>