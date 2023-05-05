<template>
    <Pie :width="300" :height="200" :data="data" :options="options" />
</template>

<script>
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'
import { Pie } from 'vue-chartjs'

ChartJS.register(ArcElement, Tooltip, Legend)
export default{
    name: 'LanguagesUsed',
    props: {
        languages_used: Object
    },
    components: {
        Pie
    },
    data(){
        return {
            data: {
                labels: Object.keys(this.languages_used),
                datasets:[
                    {
                        backgroundColor: ['#41B883', '#E46651', '#00D8FF', '#DD1B16'],
                        data: Object.values(this.languages_used)
                    }
                ]
            },
            options: {
                responsive: false,
                // maintainAspectRatio: false
            }
        }
    }
   
    /*
    methods: {
        extractData() {
            var data = {
                labels: Object.keys(this.languages_used),
                datasets:[
                    {
                        data: Object.values(this.languages_used)
                    }
                ]
            }
            var options = {
                responsive: true,
                // maintainAspectRatio: false
            }
            return [data, options]
        }
    },
    async created(){
        // var extractedData = this.extractData();
        // this.data = extractedData[0];
        // this.options = extractedData[1];
        // console.log(this.data);
    }
    */
}



</script>

<style>
</style>
