<template>
  <b-navbar toggleable="md" fixed="top" class="page-header">
    <b-container>

      <b-nav-toggle target="nav_collapse"></b-nav-toggle>

      <b-navbar-brand to="/"><img src="/wp-content/themes/vuejs-theme/dist/images/WASPN.png" alt="waspn logo" /></b-navbar-brand>

      <b-collapse is-nav id="nav_collapse">

        <!-- Right aligned nav items -->
        <b-nav is-nav-bar class="ml-auto">
          <b-nav-item href="#">Details</b-nav-item>
          <b-nav-item href="#">Accessibility</b-nav-item>
          <b-nav-item href="#">Sponsors</b-nav-item>
          <b-nav-item href="#">Contact</b-nav-item>
        </b-nav>

      </b-collapse>
    </b-container>
  </b-navbar>
</template>
