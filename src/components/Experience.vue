<template>
    <panel title="PROFESSIONAL EXPERIENCE">
        <v-card flat v-for="Experience in Experiences" :key="Experience.id" class="mx-auto">
            <v-card-title>
                <p>
                    <v-badge :value="hover" transition="slide-x-transition" color="cyan" :content="`${Experience.from} - ${Experience.to}`">
                        <v-hover v-model="hover">
                            <span class="text-h6 teal--text text--accent-4 font-weight-bold">{{Experience.title}}</span>
                        </v-hover>
                    </v-badge>
                    <br>
                    <span class="text-subtitle-2 font-weight-bold grey--text">{{Experience.organization}}</span>
                </p>        
            </v-card-title>
            <v-card-text>
                <p class="text-justify" v-html="Experience.activities"></p>
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
            hover: false,
            Experiences: [
                {id: 1, title: 'RESEARCH FELLOW', from: 'November, 2023', to: 'Present', organization: 'Robert Bosch Centre for Cyber-Physical Systems @ IISc', activities: '<ol><li>Exploring applications of geospatial data in urban planning, environmental management, and wildlife conservation.</li><li>Collaborating with multidisciplinary teams to develop solutions using geoinformatics.</li><li>Working on innovative tools for spatial analysis and decision-making support systems.</li></ol>'},
                {id: 2, title: 'EIA/EMP PROJECT INTERN', from: 'September, 2023', to: 'November, 2023', organization: 'Wildlife Institute of India', activities: '<ol><li>Developed a Wildlife Management Plan for the Naini Coal Mine in Odisha.</li><li>Conducted environmental impact assessments (EIA) and created geospatial visualizations.</li><li>Worked on integrating geospatial data for the creation of detailed management plans.</li></ol>'},
                {id: 3, title: 'LANDSCAPE ECOLOGY PROJECT INTERN', from: 'January, 2023', to: 'June, 2023', organization: 'Wildlife Institute of India', activities: '<ol><li>Modelling the distribution of wild pigs and analyzing conflict vulnerability in Tamil Nadu.</li><li>Utilized geospatial tools for habitat mapping and conflict analysis.</li><li>Created geospatial models to assess wildlife corridors and human-wildlife conflicts.</li></ol>'},
                {id: 4, title: 'LEGAL ADMINISTRATIVE ASSISTANT', from: 'June, 2020', to: 'June, 2021', organization: 'High Court of Madras', activities: '<ol><li>Assisted with legal research, RTI filings, and client documentation.</li><li>Managed records and negotiated with clients for case preparation.</li><li>Handled legal documents and filing systems for case management.</li></ol>'}
            ]
        }
    }
}
</script>
