<template>
    <v-row class="px-16">
      <v-col cols="12" md="6" class="pl-6" style="background: blue;">
          <div class="text-left font-weight-bold banner-text__tagline mt-16 pt-16">
            Good Food Us
          </div>
          <div class="text-left font-weight-bold banner-text__tagline mt-n7">
            Good Mood
          </div>
          <div style="font-size: 18px;" class="pr-16 mr-16">
            I would think that conserving our natural resources<br>
            should be a conservative position: Not to waste food, and<br>
            not to throw away a lot of the food that we buy.
          </div>
      </v-col>
      <v-col cols="12" md="6" style="background: purple;">
          asdasd
      </v-col>
    </v-row>
</template>

<script>
  export default {
    name: 'BannerSection',

    data: () => ({
      ecosystem: [
        {
          text: 'vuetify-loader',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
        },
        {
          text: 'github',
          href: 'https://github.com/vuetifyjs/vuetify',
        },
        {
          text: 'awesome-vuetify',
          href: 'https://github.com/vuetifyjs/awesome-vuetify',
        },
      ],
      importantLinks: [
        {
          text: 'Documentation',
          href: 'https://vuetifyjs.com',
        },
        {
          text: 'Chat',
          href: 'https://community.vuetifyjs.com',
        },
        {
          text: 'Made with Vuetify',
          href: 'https://madewithvuejs.com/vuetify',
        },
        {
          text: 'Twitter',
          href: 'https://twitter.com/vuetifyjs',
        },
        {
          text: 'Articles',
          href: 'https://medium.com/vuetify',
        },
      ],
      whatsNext: [
        {
          text: 'Explore components',
          href: 'https://vuetifyjs.com/components/api-explorer',
        },
        {
          text: 'Select a layout',
          href: 'https://vuetifyjs.com/getting-started/pre-made-layouts',
        },
        {
          text: 'Frequently Asked Questions',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
        },
      ],
    }),
  }
</script>
