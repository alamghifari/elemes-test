<template>
    <v-row no-gutters class="px-lg-16">
        <v-col cols="12" md="6" class="pl-6">
            <div class="text-left font-weight-bold banner-text__tagline mt-lg-16 mt-5 pt-10">
            Good Food Us
            </div>
            <div class="text-left font-weight-bold banner-text__tagline mt-lg-n7 mt-n2">
            Good Mood
            </div>
            <div 
                style="
                    border-radius:50%;
                    background:#f7f7f7;
                    width: 200px;
                " 
                class="px-10 mr-14 hidden-sm-and-up">
                <v-img
                    :src="require('../assets/salad.png')"
                    contain
                    height="200"
                />
            </div>
            <div style="font-size: 15px;" class="pr-16 mr-16 my-5 hidden-sm-and-up">
            I would think that conserving our natural resources
            should be a conservative position: Not to waste food, and
            not to throw away a lot of the food that we buy.
            </div>
            <div style="font-size: 18px;" class="pr-16 mr-16 my-5 hidden-sm-and-down">
            I would think that conserving our natural resources <br>
            should be a conservative position: Not to waste food, and <br>
            not to throw away a lot of the food that we buy.
            </div>
            <div class="mt-10">
            <v-btn
                rounded
                color="#8BAC3E"
                :large="$vuetify.breakpoint.mdAndUp"
                :small="$vuetify.breakpoint.smAndDown"
                dark
                elevation="7"
                class="normal"
            >
                Daftar Sekarang
            </v-btn>
            <v-btn
                rounded
                :large="$vuetify.breakpoint.mdAndUp"
                :small="$vuetify.breakpoint.smAndDown"
                elevation="0"
                class="normal ml-3"
            >
                About Us
            </v-btn>
            </div>
        </v-col>
        <v-col cols="12" md="6">
            <v-card
                class="d-flex justify-end mb-6"
                flat
            >
                <div 
                    style="
                        border-radius:50%;
                        background:#f7f7f7;
                        width: 518x;
                    " 
                    class="px-10 mr-14 hidden-sm-and-down">
                    <v-img
                        :src="require('../assets/salad.png')"
                        contain
                        height="518"
                    />
                </div>

                <v-img
                    :src="require('../assets/cardProfile.png')"
                    contain
                    class="banner-small-image"
                    :opacity="0.5"
                    height="518"
                />
            </v-card>
        </v-col>
    </v-row>
</template>
<script>
    export default {
        name: 'BannerSection',

        data: () => ({
        
        }),
    }
</script>