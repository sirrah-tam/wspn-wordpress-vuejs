<template lang="html">
  <b-jumbotron id="accessibility" class="text-white" bg-variant="secondary">
    <div class="section-content">
      <h2>Accessibility</h2>
      <hr>
      <div class="accessibility__content" v-html="pageContent.content.rendered">

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
        return this.page('accessibility')
      }
    }
}
</script>
