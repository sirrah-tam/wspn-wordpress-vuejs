<template>
  <b-container class="py-5">
    <template v-if="allPagesLoaded">
      <b-jumbotron class="home text-center" :style="{ backgroundImage: `url(${ featuredmedia })` }">
        <div class="page-content" v-html="pageContent.content.rendered">

        </div>
      </b-jumbotron>

      <app-details></app-details>
      <app-accessibility></app-accessibility>
      <app-sponsors></app-sponsors>
      <app-contact></app-contact>
    </template>
  </b-container>
</template>

<script>
import { mapGetters } from 'vuex'
import Details from './sections/Details'
import Accessibility from './sections/Accessibility'
import Sponsors from './sections/Sponsors'
import Contact from './sections/Contact'

export default {
  components: {
    appDetails: Details,
    appAccessibility: Accessibility,
    appSponsors: Sponsors,
    appContact: Contact
  },

  computed: {
    ...mapGetters({
      page: 'page',
      allPagesLoaded: 'allPagesLoaded'
    }),

    pageContent() {
      return this.page('home')
    },

    featuredmedia() {
      return this.pageContent._embedded['wp:featuredmedia'][0]['source_url']
    }
  },

  // Grab image and save as either computed or data property, then do v-if on if its set
}
</script>
