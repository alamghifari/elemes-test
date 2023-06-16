<template>
    <v-app>
        <HeaderSection />
        <v-main>
            <BannerSection />
            <CategorySection />
            <TrendingSection />
        </v-main>
    </v-app>
</template>

<script>
import HeaderSection from './components/HeaderSection';
import BannerSection from './components/BannerSection';
import CategorySection from './components/CategorySection';
import TrendingSection from './components/TrendingSection';

export default {
    name: 'App',

    components: {
        HeaderSection,
        BannerSection,
        CategorySection,
        TrendingSection
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
    .card-with-background {
        background: url('./assets/bg-button.png');
        position: relative;
    }
    .v-slide-group__next{
        background: #8BAC3E;
        height: 50px;
        width: 113px;
        color: white;
        border-radius: 100px;
        position: absolute;
        bottom: -40px;
        right: 20px;
    }
    .v-slide-group__prev{
        background: #8BAC3E;
        height: 50px;
        width: 113px;
        color: white;
        border-radius: 100px;
        position: absolute;
        bottom: -40px;
        right: 150px;
    }
</style>
