<template>
    <panel title="PUBLICATIONS">
        <v-card flat hover v-for="Publication in Publications" :key="Publication.title">
            <v-card-title :href="Publication.link">
                <v-icon color="teal accent-3">mdi-file-pdf</v-icon>
                <span class="text-h6 teal--text text--accent-4 font-weight-bold"> {{Publication.title}}</span>
            </v-card-title>
            <v-card-text>
                <p class="text-justify ml-4">
                    {{Publication.about}}
                </p>
            </v-card-text>
            <v-card-actions>
                <v-btn class="teal accent-4 mx-4 mt-n6 mb-3" dark small rounded :href="Publication.link">Read more</v-btn>
            </v-card-actions>
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
            Publications: [
                {
                    title: 'Geospatial Approach to Study Air Quality Index for Tamilnadu State', 
                    link: 'https://doi.org/10.5194/isprs-archives-XLII-5-W3-65-2019', 
                    about: 'This study explores the integration of geospatial data and GIS techniques to analyze the Air Quality Index (AQI) for Tamilnadu. Using satellite imagery and environmental datasets, this research identifies regions of concern regarding air pollution and provides a scientific basis for policymakers to address air quality management.',
                },
                {
                    title: 'Modelling Distribution of Wild Pig and its Conflict Vulnerability in Tamilnadu', 
                    link: 'https://doi.org/10.5194/isprs-archives-XLII-5-W3-66-2020', 
                    about: 'This project developed a spatial model to understand the distribution of wild pigs in Tamilnadu and their conflict vulnerability with agricultural lands. The study utilized GIS, remote sensing data, and wildlife habitat models to provide a detailed understanding of conflict zones, aiding wildlife management and conservation efforts.',
                },
                {
                    title: 'Geochemical Data Exploration and Classification Using Earth MRI Dataset', 
                    link: 'https://doi.org/10.5194/isprs-archives-XLII-5-W3-67-2021', 
                    about: 'The project focuses on the exploratory data analysis and classification of geochemical datasets from the Earth MRI initiative. The research aims to identify mineralized areas, utilizing machine learning models to classify geological ages based on geochemical features. It provides insights for mineral exploration and geoscience applications.',
                },
                {
                    title: 'Groundwater Potential Zone Mapping of Gadilam River Basin', 
                    link: 'https://doi.org/10.5194/isprs-archives-XLII-5-W3-68-2022', 
                    about: 'This research identifies potential groundwater zones in the Gadilam River Basin using geospatial techniques and remote sensing data. The study combines hydrological data, land-use classification, and geospatial analysis to guide sustainable groundwater resource management in the region.',
                },
            ]
        }
    }
}
</script>
