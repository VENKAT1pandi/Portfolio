<template>
    <panel title="AWARDS">
        <v-card flat v-for="Award in Awards" :key="Award.title">
            <v-card-text class="ml-4">
                <v-icon color="teal accent-4">mdi-{{Award.icon}} </v-icon>
                <span class="grey--text text--darken-2"> {{Award.title}}</span>
            </v-card-text>
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
            Awards: [
                {title: 'Pre-doctoral fellowship from Kotak Mahindra Bank', icon: 'medal'},
                {title: 'Honored with C1 Advanced Certificate by EF Education First', icon: 'certificate'},
                {title: 'Classifying Objects Using Deep Learning in ArcGIS Pro by Esri', icon: 'trophy-award'},
                {title: 'Nature-based Solutions for Disaster and Climate Resilience by PEDRR', icon: 'leaf'},
            ]
        }
    }
}
</script>