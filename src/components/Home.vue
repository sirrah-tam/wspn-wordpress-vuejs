<template>
  <b-container class="py-5">
    <template v-if="allPagesLoaded">
      <b-jumbotron class="home text-center" :style="{ backgroundImage: `url('${pageContent._embedded['wp:featuredmedia'][0]['source_url']}')` }">
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
    }
  },
}
</script>
