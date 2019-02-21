<template>
    <div>
            <Tab v-bind:tabTitles=tabs v-bind:toolbarTitle="title"></Tab>
    </div>
</template>

<script>
    import Tab from "@/components/Tab";
    import DataTable from "@/components/DataTable";
    import {HEADERS} from "@/constants";
    import {USER_STORIES} from "@/constants";
    import {PROCESSES} from "@/constants";
    import {GRADIENT} from "@/constants";
    import CircleChart from "@/components/CircleChart";
    import SparkLine from "@/components/SparkLine";
    import BarChart from "@/components/BarChart";
    export default {
        name: "Github",
        components: {Tab},
        data() {
            return {
                title: "Github Statistic",
                tabs: {
                    'Commits': {data: USER_STORIES, component: xcircle, headers: HEADERS, title: 'Commits in Tasks'},
                    'Contribution': {data: PROCESSES, component: xhbar, title: 'Contributions', headers: null},
                    'Process': {data: PROCESSES, component: xline, title: 'User Stories', headers: null},
                    'Burn Down Chart': {data: GRADIENT, component: SparkLine, title: 'Burn Down Chart', headers: null},
                }
            }
        }
    }
</script>

