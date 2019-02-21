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
    import xline from "@/components/xline";
    import xhbar from "@/components/xhbar";
    
    export default {
        name: "Github",
        components: {Tab},
        data() {
            return {
                title: "Github Statistic",
                tabs: {
                    'Commits': {data: USER_STORIES, component: DataTable, headers: HEADERS, title: 'Commits during the development'},
                    'Contribution': {data: PROCESSES, component: xhbar, title: 'Contributions', headers: null},
                    'Process': {data: PROCESSES, component: xline, title: 'User Stories', headers: null},
                }
            }
        }
    }
</script>


