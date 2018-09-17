<template>
  <b-container class="bv-example-row">
    <template v-if="allPagesLoaded">
      <b-jumbotron :header="pageContent.title.rendered" class="text-center">
        <div class="page-content" v-html="pageContent.content.rendered">

        </div>
      </b-jumbotron>
    </template>
  </b-container>
</template>

<script>
import { mapGetters } from 'vuex'
import Details from './partials/Details'
import Sponsors from './partials/Sponsors'
import Contact from './partials/Contact'

export default {
  components: {
    Details,
    Sponsors,
    Contact
  },

  computed: {
    ...mapGetters({
      page: 'page',
      allPagesLoaded: 'allPagesLoaded'
    }),

    pageContent() {
      return this.page('home-main')
    }
  },
}
</script>

<style lang="scss">
.jumbotron {
  margin-top: 5%;
}
</style>
