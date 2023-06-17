<template>
    <div>
        <v-footer 
            padless
            class="hidden-sm-and-up"
            color="white"
        >
            <v-col
                class="text-center"
                cols="4"
            >
                <v-card
                    class="d-flex justify-center text-center ma-2"
                    width="230"
                    elevation="0"
                >
                    <v-row class="text-center">
                        <v-col cols="12">
                            <v-icon large class="mb-2">mdi-menu</v-icon>
                            <span class="d-block">Home</span>
                        </v-col>
                    </v-row>
                </v-card>
            </v-col>
            <v-col
                class="text-center"
                cols="4"
            >
                <v-card
                    class="d-flex justify-center text-center ma-2"
                    width="230"
                    elevation="0"
                >
                    <v-row class="text-center">
                        <v-col cols="12">
                            <v-icon large class="mb-2">mdi-menu</v-icon>
                            <span class="d-block">Promotions</span>
                        </v-col>
                    </v-row>
                </v-card>
            </v-col>
            <v-col
                class="text-center"
                cols="4"
            >
                <v-card
                    class="d-flex justify-center text-center ma-2"
                    width="230"
                    elevation="0"
                >
                    <v-row class="text-center">
                        <v-col cols="12">
                            <v-icon large class="mb-2">mdi-menu</v-icon>
                            <span class="d-block">Others</span>
                        </v-col>
                    </v-row>
                </v-card>
            </v-col>
        </v-footer>
        <v-footer
            padless
            class="pa-16 hidden-sm-and-down"
            color="white"
        >
            <v-card
                flat
                tile
                width="100%"
                color="#F9FFF6"
            >   
                <v-row class="pt-6">
                    <v-col cols="4">
                        <v-img
                            :src="require('../assets/eleme.png')"
                            contain
                            style="position: absolute;left: 4%;top: 50px;"
                            height="50"
                        />
                        <div class="pt-5">
                            <v-card-text class="mt-16 pl-14">
                                Jl. Prof. DR. Satrio No.7, RT.3/RW.3, Karet Kuningan, 
                                Kecamatan Setiabudi, Kota Jakarta Selatan, <br>
                                Daerah Khusus Ibukota Jakarta 12950
                            </v-card-text>
                            <v-row
                                align="center"
                                justify="space-around"
                            >
                                <v-col cols="1"></v-col>
                                <v-col cols="1">
                                    <v-hover v-slot="{ hover }">
                                        <v-btn 
                                            class="ma-2" 
                                            fab small
                                            :color="hover ? '#8BAC3E' : 'white'"
                                            elevation="0"
                                        >
                                            <v-icon  
                                                :color="hover ? 'white' : '#8BAC3E'"
                                                md
                                            >mdi-email-outline</v-icon>
                                        </v-btn>
                                    </v-hover>
                                </v-col>
                                <v-col cols="1">
                                    <v-hover v-slot="{ hover }">
                                        <v-btn 
                                            class="ma-2" 
                                            fab small
                                            :color="hover ? '#8BAC3E' : 'white'"
                                            elevation="0"
                                        >
                                            <v-icon  
                                                :color="hover ? 'white' : '#8BAC3E'"
                                                md
                                                >mdi-phone-outline</v-icon>
                                        </v-btn>
                                    </v-hover>
                                </v-col>
                                <v-col cols="1">
                                    <v-hover v-slot="{ hover }">
                                        <v-btn 
                                            class="ma-2" 
                                            fab small
                                            :color="hover ? '#8BAC3E' : 'white'"
                                            elevation="0"
                                        >
                                            <v-icon  
                                                :color="hover ? 'white' : '#8BAC3E'"
                                                md
                                                >mdi-instagram</v-icon>
                                        </v-btn>
                                    </v-hover>
                                </v-col>
                                <v-col cols="8"></v-col>
                            </v-row>
                        </div>
                    </v-col>
                    <v-col cols="2">
                        <v-card-title>
                            Categories
                        </v-card-title>
                        <v-row class="ml-1"
                            v-for="(item, index) in items" 
                            :key="index"
                        >
                            <v-col cols="12">
                                <div  @click="() => redirectToUrl(item.url)">{{ item.name }}</div>
                            </v-col>
                        </v-row>
                    </v-col>
                    <v-col cols="2">
                        <v-card-title>
                            About Us
                        </v-card-title>
                        <v-row class="ml-1"
                            v-for="(about, index) in abouts" 
                            :key="index"
                        >
                            <v-col cols="12">
                                <div  @click="() => redirectToUrl(about.url)">{{ about.name }}</div>
                            </v-col>
                        </v-row>
                    </v-col>
                    <v-col cols="4">
                        <v-card-title>
                            Newsletter
                        </v-card-title>
                        <v-card-text>
                            Get now free 50% discount for alll products on your first order
                        </v-card-text>
                        <v-row align="center">
                            <v-col cols="9" class="pl-6">
                                <v-text-field
                                    v-model="email"
                                    label="Email Address"
                                    outlined
                                    style="border-radius: 10px;"
                                    placeholder="Enter your email"
                                ></v-text-field>
                            </v-col>
                            <v-col cols="3">
                                <v-btn
                                    style="border-radius: 0px 10px 10px 0px;"
                                    color="#8BAC3E"
                                    class="mt-n8 ml-n16"
                                    height="56px"
                                    dark
                                    @click="submitForm"
                                >
                                    Send
                                </v-btn>
                            </v-col>
                        </v-row>
                        <v-card-text class="mt-n5">
                            <v-icon 
                                color="#8BAC3E" 
                                md
                            >mdi-email-outline</v-icon>
                            elemesid@gmail.com
                        </v-card-text>
                        <v-card-text class="mt-n5">
                            <v-icon 
                                color="#8BAC3E" 
                                md
                            >mdi-phone-outline</v-icon>
                            0888 1111 2222 
                        </v-card-text>
                    </v-col>
                </v-row>
            
            </v-card>
        </v-footer>
    </div>
</template>
<script>
    export default {
        name: 'HeaderSection',

        data: () => ({
            email: '',
            isHover: false,
            items: [
                {
                    name: 'Cupcake',
                    url: '' 
                },
                {
                    name: 'Pizza',
                    url: '' 
                },
                {
                    name: 'Kebab',
                    url: '' 
                },
                {
                    name: 'Salmon',
                    url: '' 
                },
                {
                    name: 'Dougnut',
                    url: '' 
                }
            ],
            abouts: [
                {
                    name: 'About Us',
                    url: '' 
                },
                {
                    name: 'FAQ',
                    url: '' 
                },
                {
                    name: 'Report Problem',
                    url: '' 
                }
            ]
        }),
        methods: {
            redirectToUrl(val) {
                window.location.href = val;
            },
            submitForm() {
                // Add your form submission logic here
                console.log('Email:', this.email);
            },
        },
        computed: {
            emailIsValid() {
            // Add your email validation logic here
            // For example, using a regular expression
            const emailRegex = /^\w+([-+.']\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;
            return emailRegex.test(this.email);
            },
        },
    }
</script>
<style>
    .btn-off {
        color: red
    }
    .btn-on {
        color: blue
    }
</style>
