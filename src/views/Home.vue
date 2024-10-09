<template>
    <v-container class="mx-auto">
        <v-timeline reverse :dense="$vuetify.breakpoint.smAndDown">
            <v-timeline-item
                v-for="Time in Timeline"
                :key="Time.id"
                :color="Time.color"
                :icon="Time.icon"
                fill-dot
            >
                <template v-slot:opposite>
                    <span
                        :class="`text-body-2 font-weight-bold ${Time.color}--text`"
                        v-text="Time.at"
                    >
                    </span>
                </template>
                <v-card>
                    <v-card-title
                        :class="`${Time.color} ${Time.justify}`"
                    >
                        <v-icon class="mx-2" dark>
                            {{Time.icon}}
                        </v-icon>
                        <h2 class="text-h6 white--text font-weight-light">{{Time.title}}</h2>
                    </v-card-title>
                    <v-card-text v-html="Time.description">
                    </v-card-text>
                </v-card>
            </v-timeline-item>
        </v-timeline>
    </v-container>
</template>

<script>

export default {
    components: {
    },
    data() {
        return {
            Timeline: [
                {
                    id: '1', color: 'blue', icon: 'mdi-school', at: 'May, 2024', justify: 'justify-start',
                    title: 'Exec. Certificate in Finance',
                    description: 'Pursuing an Executive Certificate in Corporate & Strategic Finance at Indian Institute of Management Mumbai.'
                },
                {
                    id: '2', color: 'purple', icon: 'mdi-laptop', at: 'Nov, 2023', justify: 'justify-end',
                    title: 'Research Fellow @ IISc',
                    description: 'Joined Robert Bosch Centre for Cyber-Physical Systems @ IISc as a Research Fellow, focusing on geospatial data applications for urban planning, environmental management, and wildlife conservation.'
                },
                {
                    id: '3', color: 'green', icon: 'mdi-certificate', at: 'Jul, 2023', justify: 'justify-start',
                    title: 'C1 Advanced Cert.',
                    description: 'Received C1 Advanced Certificate from EF Education First.'
                },
                {
                    id: '4', color: 'amber', icon: 'mdi-school', at: 'Jul, 2023', justify: 'justify-end',
                    title: 'MTech in Geoinformatics',
                    description: 'Completed MTech in Geoinformatics from Bharathidasan University, Tiruchirappalli, gaining expertise in geospatial science.'
                },
                {
                    id: '5', color: 'cyan', icon: 'mdi-laptop', at: 'Sep, 2023', justify: 'justify-start',
                    title: 'EIA/EMP Intern',
                    description: 'Interned at Wildlife Institute of India, focusing on the Environmental Impact Assessment for Naini Coal Mines, Odisha.'
                },
                {
                    id: '6', color: 'indigo', icon: 'mdi-laptop', at: 'Jan, 2023', justify: 'justify-end',
                    title: 'Landscape Ecology Intern',
                    description: 'Developed wildlife management plans and modeled wild pig distribution in Tamil Nadu during my internship at Wildlife Institute of India.'
                },
                {
                    id: '7', color: 'red', icon: 'mdi-gavel', at: 'Jun, 2020', justify: 'justify-start',
                    title: 'Legal Asst. @ High Court',
                    description: 'Assisted legal research, filing RTIs, and documentation at the High Court of Madras.'
                },
                {
                    id: '8', color: 'purple', icon: 'mdi-book-open', at: 'Dec, 2022', justify: 'justify-end',
                    title: 'Air Quality Study',
                    description: 'Conducted a geospatial study of Air Quality Index for Tamil Nadu, associated with Bharathidasan University.'
                }
            ]
        }
    }
}
</script>
