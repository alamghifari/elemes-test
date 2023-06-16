<template>
    <v-row no-gutters class="px-lg-16 px-6 mt-16">
        <v-col cols="12" class="pl-lg-6">
            <h1 class="content-title">Browser Our Category</h1> 
            <h1 class="content-title content-text__green">Receipt</h1> 
        </v-col>
        <v-col cols="12" class="px-lg-4 mt-10">
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
                            :color="item.color"
                            class="d-flex justify-center text-center ma-2"
                            :class="hover ? 'card-with-background' : ''"
                            :height="hover ? 195 : 175"
                            width="230"
                        >
                            <v-row class="text-center">
                                <v-col cols="12">
                                    <v-img
                                        :src="item.img ? require(`../assets/${item.img}`) : ''"
                                        contain
                                        class="mb-3 mt-8"
                                        height="60"
                                    />
                                    <b>{{ item.name }}</b><br>
                                    {{ item.qty }} Items
                                </v-col>
                            </v-row>
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
            model: '',
            items: [
                {
                    id: 1,
                    img:'cupcake.png',
                    name: 'Cupcake',
                    color: '#F0FEEB',
                    qty: 22
                },
                {
                    id: 2,
                    img:'pizza.png',
                    name: 'Pizza',
                    color: '#E6F3F5',
                    qty: 25
                },
                {
                    id: 3,
                    img:'kebab.png',
                    name: 'Kebab',
                    color: '#EAEEFA',
                    qty: 12
                },
                {
                    id: 4,
                    img:'salmon.png',
                    name: 'Salmon',
                    color: '#F9EEF3',
                    qty: 22
                },
                {
                    id: 5,
                    img:'doughnut.png',
                    name: 'Doughnut',
                    color: '#F3F7D9',
                    qty: 11
                },
                {
                    id: 6,
                    img:'cupcake.png',
                    name: 'Organic Cupcake',
                    color: '#F9EEF3',
                    qty: 12
                },
                {
                    id: 7,
                    img:'pizza.png',
                    name: 'American Pizza',
                    color: '#EAEEFA',
                    qty: 20
                },
                {
                    id: 8,
                    img:'kebab.png',
                    name: 'Organic Kebab',
                    color: '#F3F7D9',
                    qty: 12
                },
            ]
        }),
        methods: {

        }
    }
</script>
<style>
    
</style>