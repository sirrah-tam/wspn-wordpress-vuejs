<template lang="html">
  <div id="contact" class="text-white">
    <h2>Contact</h2>
    <div class="details__content" v-html="pageContent.content.rendered">

    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {

    computed: {
      ...mapGetters({
        page: 'page'
      }),

      pageContent() {
        return this.page('contact')
      }
    }
}
</script>
