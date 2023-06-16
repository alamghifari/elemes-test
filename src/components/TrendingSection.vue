<template>
    <v-row no-gutters class="px-lg-16 px-6 my-16">
        <v-col cols="12" class="pl-lg-6">
            <h1 class="content-title">Browser Our Tranding</h1> 
            <h1 class="content-title content-text__green">Receipt</h1> 
        </v-col>
        <v-col cols="12" class="mt-10">
            <v-row>
                <v-col v-for="(item, index) in items" :key="index" cols="3">
                    <v-card
                        class="mx-lg-6 pt-5 pl-lg-2"
                        style="border-radius: 10px;"
                        :color="item.color"
                        width="287"
                        height="306"
                    >
                        <v-img
                            height="120"
                            width="120"
                            class="ml-lg-3"
                            style="border-radius: 0px;"
                            src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                        ></v-img>
                        <v-card-title>Cafe Badilico</v-card-title>
                        <v-card-text class="mt-n3">
                            Italian, Cafe
                            <v-rating
                                :value="4.5"
                                color="amber"
                                class="mt-2"
                                dense
                                half-increments
                                readonly
                                size="14"
                            ></v-rating>
                        </v-card-text>
                    </v-card>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>
<script>
    export default {
        name: 'TrendingSection',

        data: () => ({
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
    }
</script>