<template lang="html">
  <b-jumbotron id="details" class="" bg-variant="secondary">
    <div class="section-content">
      <h2>Details</h2>
      <hr>
      <div class="details__content" v-html="pageContent.content.rendered">

      </div>
      <hr>
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
