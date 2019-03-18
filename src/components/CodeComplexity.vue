<template>
    <div>
        <vue-easy-pie-chart :percent="70"></vue-easy-pie-chart>
        <vue-easy-pie-chart :percent="90"></vue-easy-pie-chart>
        <vue-easy-pie-chart :percent="60"></vue-easy-pie-chart>
        <vue-easy-pie-chart :percent="75"></vue-easy-pie-chart>
        <vue-easy-pie-chart :percent="68"></vue-easy-pie-chart>
    </div>
</template>

<script>
    import VueEasyPieChart from 'vue-easy-pie-chart'
    import 'vue-easy-pie-chart/dist/vue-easy-pie-chart.css'

    export default {
        components:{ VueEasyPieChart }
    }
</script>