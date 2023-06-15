<template>
    <v-app-bar
        app
        flat
        color="white"
        class="px-lg-16 px-md-3 px-0"
    >
        <div class="d-flex align-center">
            <v-img
                :src="require('../assets/eleme.png')"
                class="my-3 hidden-sm-and-down"
                contain
                height="200"
            />
            <v-img
                :src="require('../assets/eleme.png')"
                class="my-3 hidden-md-and-up"
                contain
                height="40"
            />
        </div>

        <v-spacer></v-spacer>
        <div class="hidden-sm-and-down" style="background: red;">
            <v-btn text class="normal">
                Home
            </v-btn>
            <v-btn text class="normal">
                About
            </v-btn>
            <v-btn text class="normal">
                Promotion
            </v-btn>
            <v-btn text class="normal">
                Blogs
            </v-btn>
            <v-btn text class="normal">
                Contact Us
            </v-btn>
        </div>
        <v-spacer></v-spacer>
        <div>
            <v-btn text class="normal hidden-sm-and-down">
                Masuk
            </v-btn>
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
        </div>
    </v-app-bar>
</template>
  
<script>
    export default {
        name: 'HeaderSection',

        data: () => ({
        
        }),
    }
</script>
