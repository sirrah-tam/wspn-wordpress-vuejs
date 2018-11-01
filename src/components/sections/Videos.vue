<template lang="html">
  <b-jumbotron id="videos" class="videos my-3" bg-variant="secondary">
    <h2 class="mb-5 text-center">Videos</h2>
    <div class="details__content" v-html="pageContent.content.rendered">

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
        return this.page('videos')
      }
    }
}
</script>
