<template>
    <panel title="PROJECTS">
        <v-card flat v-for="Project in Projects" :key="Project.title" hover ripple>
            <v-card-title>
                <span class="text-h6 teal--text text--accent-4 font-weight-bold">{{Project.title}}</span>
            </v-card-title>
            <v-card-text>
                <p class="text-justify ml-4 ">
                    {{Project.description}}
                </p>
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
        return{
            Projects: [
                {title: 'Geochemical Data Exploration and Classification Using Earth MRI Dataset', description: 'This project involves an extensive exploratory data analysis (EDA) and classification of geochemical data from the Earth Mapping Resources Initiative (Earth MRI) dataset. The aim is to identify mineralized areas containing critical minerals using machine learning models to classify geological ages based on geochemical features.'},
                {title: 'Deciphering City Outcomes through Data Exploration - DeCODE Challenge 2023', description: 'This project focuses on analyzing city-level data to understand urban outcomes and challenges using advanced geospatial and data science techniques. The project involves using tools like AWS, ArcGIS, and Google Earth Engine to extract meaningful insights and develop solutions.'},
                {title: 'Dulung-Subansri Rapid Elephant Assessment for NHPC Lower Subansri Dam', description: 'As part of the Wildlife Institute of India, this project involved assessing elephant movement patterns and conflict vulnerability around the Lower Subansri Dam in Assam. The project utilized GIS tools like GeoServer, TensorFlow, and Quantum GIS to create a conservation plan for mitigating human-elephant conflict.'},
                {title: 'Modelling Distribution of Wild Pig Conflict Vulnerability in Tamilnadu', description: 'This project involved modeling the spatial distribution of wild pig populations and their conflict vulnerability using geospatial tools like Google Earth Engine, R, and ArcGIS. The model helped identify high-risk zones to inform wildlife management strategies.'},
                {title: 'Geospatial Approach to Study Air Quality Index for Tamilnadu State', description: 'This project focused on analyzing air quality in Tamilnadu using geospatial data and remote sensing techniques. Tools like Google Earth Engine, AWS, and Python were used to map air quality trends and assess environmental impacts.'}
            ]
        }
    }
}
</script>
