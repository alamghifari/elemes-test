<template>
    <v-app>
        <HeaderSection />
        <v-main>
            <BannerSection />
            <CategorySection />
            <TrendingSection />
            <!-- <HelloWorld /> -->
        </v-main>
    </v-app>
</template>

<script>
import HeaderSection from './components/HeaderSection';
import BannerSection from './components/BannerSection';
import CategorySection from './components/CategorySection';
import TrendingSection from './components/TrendingSection';
// import HelloWorld from './components/HelloWorld';

export default {
    name: 'App',

    components: {
        HeaderSection,
        BannerSection,
        CategorySection,
        TrendingSection,
        // HelloWorld,
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
.content-text__green {
    color: #8BAC3E;
}
.content-title {
    font-size: 40px;
}
</style>
