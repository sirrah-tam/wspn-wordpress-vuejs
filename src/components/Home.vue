<template>
  <b-container class="py-5">
    <template v-if="allPagesLoaded">
      <b-jumbotron class="text-center">
        <div class="page-content" v-html="pageContent.content.rendered">

        </div>
      </b-jumbotron>

      <app-details></app-details>
      <app-sponsors></app-sponsors>
      <app-Contact></app-contact>
    </template>
  </b-container>
</template>

<script>
import { mapGetters } from 'vuex'
import Details from './sections/Details'
import Sponsors from './sections/Sponsors'
import Contact from './sections/Contact'

export default {
  components: {
    appDetails: Details,
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
