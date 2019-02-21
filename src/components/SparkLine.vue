<template>
    <v-card height="50%"  py-0 px-2>
        <v-container width="90%">
            <v-layout justify-center>
                <v-card-title primary-title>
                    <div>
                        <h3 class="headline mb-0 orange&#45;&#45;text">{{ title }}</h3>
                    </div>
                </v-card-title>
            </v-layout>
            <v-container fluid>
                <v-sparkline
                        :value="[25, 18, 15, 12, 12, 17, 4, 4, 0, 1, 0, 0]"
                        :gradient="data[5]"
                        :smooth="1 || false"
                        :padding="8"
                        :line-width="2"
                        :stroke-linecap="'round'"
                        :gradient-direction="'top'"
                        auto-draw
                ></v-sparkline>
                <v-divider></v-divider>
            </v-container>
            <v-layout align-center justify-space-around row fill-height>
                <p v-for="(proc, index) in [23, 18, 14, 11, 12, 10, 7, 5, 1, 2, 0, 0]"
                   :key="proc">day {{index+1}}</p>
            </v-layout>
        </v-container>
    </v-card>
</template>

<script>
    export default {
        name: "SparkLine",
        props: ["data", "headers", "title"],
    }
</script>
