<template>
    <v-row no-gutters class="px-lg-16 px-6 my-16">
        <v-col cols="12" class="pl-lg-6">
            <h1 class="content-title">Browser Our Tranding</h1> 
            <h1 class="content-title content-text__green">Receipt</h1> 
        </v-col>
        <v-col cols="12" class="mt-10">
            <v-row>
                <v-col v-for="(item, index) in items" :key="index" cols="12" lg="3" class="d-flex justify-center">
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
                            :src="item.img ? require(`../assets/${item.img}`) : ''"
                        ></v-img>
                        <v-card-title>{{ item.name }}</v-card-title>
                        <v-card-text class="mt-n3">
                            {{ item.text }}
                            <v-rating
                                :value="item.rating"
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
            <v-row class="text-center">
                <v-col class="my-6">
                    <v-btn
                        rounded
                        color="#8BAC3E"
                        :large="$vuetify.breakpoint.mdAndUp"
                        :small="$vuetify.breakpoint.smAndDown"
                        dark
                        class="normal"
                    >
                        Daftar Sekarang
                    </v-btn>
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
                    img:'1.png',
                    name: 'Pizza Paperoni',
                    color: '#E6F3F5',
                    text: 'Pizza',
                    rating: 4
                },
                {
                    id: 2,
                    img:'2.png',
                    name: 'Pizza Meat',
                    color: '#E6F3F5',
                    text: 'Pizza',
                    rating: 3
                },
                {
                    id: 3,
                    img:'3.png',
                    name: 'Doner Kebab',
                    color: '#EAEEFA',
                    text: 'Pizza',
                    rating: 5
                },
                {
                    id: 4,
                    img:'4.png',
                    name: 'Salmon Roll',
                    color: '#F9EEF3',
                    text: 'Pizza',
                    rating: 4
                },
                {
                    id: 5,
                    img:'5.png',
                    name: 'Cupcake Choco',
                    color: '#F0FEEB',
                    text: 'Pizza',
                    rating: 4
                },
                {
                    id: 6,
                    img:'6.png',
                    name: 'Doughnut Milk',
                    color: '#F3F7D9',
                    text: 'Pizza',
                    rating: 5
                },
                {
                    id: 7,
                    img:'7.png',
                    name: 'Doughnut Unicorn',
                    color: '#F3F7D9',
                    text: 'Pizza',
                    rating: 4
                },
                {
                    id: 8,
                    img:'8.png',
                    name: 'Kathi Kebab',
                    color: '#EAEEFA',
                    text: 'Pizza',
                    rating: 4
                },
            ]
        }),
    }
</script>