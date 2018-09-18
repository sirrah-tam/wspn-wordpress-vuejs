<template>
  <b-navbar toggleable="md" fixed="top" class="page-header">
    <b-container>

      <b-nav-toggle target="nav_collapse"></b-nav-toggle>

      <b-navbar-brand to="/"><img src="/wp-content/themes/wspn-wordpress-vuejs/dist/assets/WASPN.png" alt="waspn logo" /></b-navbar-brand>

      <b-collapse is-nav id="nav_collapse">

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#details" v-smooth-scroll="{target: '#details'}">Details</b-nav-item>
          <b-nav-item href="#">Accessibility</b-nav-item>
          <b-nav-item href="#sponsors" v-smooth-scroll>Sponsors</b-nav-item>
          <b-nav-item href="#contact" v-smooth-scroll>Contact</b-nav-item>
        </b-navbar-nav>

      </b-collapse>
    </b-container>
  </b-navbar>
</template>
