<template lang="html">
  <b-jumbotron id="details" class="text-center text-white" bg-variant="secondary">
    <div class="page-content" v-html="pageContent.content.rendered">
      <h2>Details</h2>
      <div class="details__content" v-html="pageContent.content.rendered">

      </div>
    </div>
  </b-jumbotron>
</template>

<script>
import { mapGetters } from 'vuex'
export default {

    computed: {
      ...mapGetters({
        page: 'page'
      }),

      pageContent() {
        return this.page('details')
      }
    }
}
</script>
