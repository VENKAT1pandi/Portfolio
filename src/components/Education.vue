<template>
    <panel title="ACADEMIC BACKGROUND">
        <v-card v-for="Academic in Academics" :key="Academic.degree" flat class="px-2" :color="`${Academic.color} lighten-5`">
            <v-row :class="`${Academic.degreeId} px-2`">
                <v-row>
                    <v-col xs12 sm6 md3>
                        <div class="text-caption blue--text text-center">
                            Degree
                        </div>
                        <div class="text-subtitle-1 font-weight-bold grey--text text--darken-1">
                            {{Academic.degree}}
                        </div>
                    </v-col>
                    <v-col xs12 sm6 md3>
                        <div class="text-caption deep-purple--text text--lighten-1 text-center">
                            College
                        </div>
                        <div class="text-subtitle-1 font-weight-bold grey--text text--darken-1">
                            {{Academic.college}}
                        </div>
                    </v-col>
                    <v-col xs12 sm6 md2>
                        <div class="text-caption light-green--text text--darken-3 text-center">
                            Period (In A.D.)
                        </div>
                        <div class="text-subtitle-1 font-weight-bold grey--text text--darken-1 text-center">
                            {{Academic.periodAD}}
                        </div>
                    </v-col>
                    <v-col xs12 sm6 md2>
                        <div class="text-caption amber--text text--darken-3 text-center">
                            Status
                        </div>
                        <div align="center" class="mt-3">
                            <v-chip small dark :color="`${Academic.color}`">
                                {{Academic.status}}
                            </v-chip>
                        </div>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col xs12 sm6 md2>
                        <div class="text-caption teal--text text--darken-2 text-center">
                            Division
                        </div>
                        <div class="text-subtitle-1 font-weight-bold grey--text text--darken-1 text-center">
                            {{Academic.division}}
                        </div>
                    </v-col>
                    <v-col xs12 sm6 md2>
                        <div class="text-caption teal--text text--accent-4 text-center">
                            Percentage
                        </div>
                        <div class="text-subtitle-1 font-weight-bold grey--text text--darken-1 text-center">
                            {{Academic.percentage}} %
                        </div>
                    </v-col>
                    <v-col xs12 xm6 md5>
                        <div class="text-caption blue--text text--accent-3 text-center">
                            Board
                        </div>
                        <div class="text-subtitle-1 font-weight-bold grey--text text--darken-1">
                            {{Academic.board}}
                        </div>
                    </v-col>
                    <v-col xs2>
                         <div align="center">
                             <v-tooltip bottom color="indigo accent-3">
                                <template v-slot:activator="{ on }">
                                    <v-btn icon :color="`${Academic.color}`" class="ml-12" v-on="on">
                                        <v-icon>mdi-chart-areaspline</v-icon>
                                    </v-btn>
                                </template>
                                <span>View all record of {{Academic.degreeId}}</span>
                            </v-tooltip>
                        </div>
                    </v-col>
                </v-row>
            </v-row>
            <v-divider></v-divider>
        </v-card>
    </panel>
</template>

<script>
import Panel from '@/components/Panel'

export default {
    components: {
        Panel
    },
    data() {
        return {
            Academics: [
                {degreeId: 'masters', degree: 'Master of Technology (M.Tech) in Geoinformatics', college: 'Bharathidasan University, Tiruchirappalli', periodAD: '2021 - 2023', status: 'Completed', division: 'A+', percentage: '80.00', board: 'Bharathidasan University', color:'orange'},
                {degreeId: 'bachelors', degree: 'Masters of Science (5 Year Integrated) in Geology', college: 'Bharathidasan University, Tiruchirappalli', periodAD: '2015 - 2020', status: 'Completed', division: 'Distinction', percentage: '83.00', board: 'Bharathidasan University', color:'cyan'},
                {degreeId: 'pgdm', degree: 'PGDM in Corporate Finance & Strategy Management', college: 'Indian Institute of Management Mumbai', periodAD: '2023 - 2024', status: 'Ongoing', division: 'N/A', percentage: 'N/A', board: 'IIM Mumbai', color:'purple'}
            ]
        }
    }
}
</script>

<style scoped>
.masters{
    border-left: 4px solid #FF9800;
    border-right: 4px solid #FF9800;
}
.bachelors{
    border-left: 4px solid #18FFFF;
    border-right: 4px solid #18FFFF;
}
.pgdm{
    border-left: 4px solid #D500F9;
    border-right: 4px solid #D500F9;
}
</style>
