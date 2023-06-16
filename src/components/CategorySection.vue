<template>
    <v-row no-gutters class="px-lg-16 px-6 mt-16">
        <v-col cols="12" class="pl-lg-6">
            <h1 class="content-title">Browser Our Category</h1> 
            <h1 class="content-title content-text__green">Receipt</h1> 
        </v-col>
        <v-col cols="12">
            <v-slide-group
                v-model="model"
                style="height: 250px;"
                :show-arrows="$vuetify.breakpoint.mdAndUp"
            >
                <template v-slot:next>
                    <b>NEXT</b>
                    <v-icon 
                        color="white" 
                        large
                        class="mr-n4 ml-2"
                    >mdi-chevron-right-circle</v-icon>
                </template>
                <template v-slot:prev>
                    <v-icon 
                        color="white" 
                        large
                        class="ml-n4 mr-2"
                    >mdi-chevron-left-circle</v-icon>
                    <b>PREV</b>
                </template>
                <v-slide-item
                    v-for="(item, index) in items" 
                    :key="index"
                >
                    <v-hover v-slot="{ hover }">
                        <v-card
                            :color="hover ? undefined : 'grey lighten-1'"
                            class="ma-2"
                            :height="hover ? 195 : 175"
                            width="230"
                        >
                            <!-- <v-row
                                v-if="hover"
                                class="fill-height"
                                justify="center"
                                style="background: red;"
                                >
                                <v-scale-transition>
                                    
                                </v-scale-transition>
                            </v-row> -->
                        </v-card>
                    </v-hover>
                </v-slide-item>
            </v-slide-group>
        </v-col>
    </v-row>
</template>
<script>
    export default {
        name: 'CategorySection',

        data: () => ({
            items: ['1', '2', '3', '4', '5', '6', '7', '8', '9']
        }),
        methods: {

        }
    }
</script>
<style>
    .v-slide-group__next{
        background: #8BAC3E;
        height: 50px;
        width: 113px;
        color: white;
        border-radius: 100px;
        position: absolute;
        bottom: -50px;
        right: 20px;
    }
    .v-slide-group__prev{
        background: #8BAC3E;
        height: 50px;
        width: 113px;
        color: white;
        border-radius: 100px;
        position: absolute;
        bottom: -50px;
        right: 150px;
    }
</style>