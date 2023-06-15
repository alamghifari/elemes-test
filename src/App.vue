<template>
    <v-app>
        <HeaderSection />
        <v-main>
            <BannerSection />
        </v-main>
    </v-app>
</template>

<script>
import HeaderSection from './components/HeaderSection';
import BannerSection from './components/BannerSection';

export default {
    name: 'App',

    components: {
        HeaderSection,
        BannerSection,
    },

    data: () => ({
      //
    }),

    mounted() {

    },

    computed: {
        isDesktop() {
            return this.$vuetify.breakpoint.mdAndUp;
        },
        isMobile() {
            return this.$vuetify.breakpoint.xs;
        },
        isTablet() {
            return this.$vuetify.breakpoint.sm && !this.$vuetify.breakpoint.mdAndUp;
        },
    },
};
</script>
<style>
.normal {
    text-transform: none;
}
.banner-text__tagline {
    font-size: 64px;
    color: #8BAC3E;
}
</style>
