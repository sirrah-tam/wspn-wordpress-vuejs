<template>
  <b-navbar toggleable="md" fixed="top" class="page-header">
    <b-container>

      <b-navbar-brand to="/"><img src="/wp-content/themes/wspn-wordpress-vuejs/dist/assets/WASPN.png" alt="waspn logo" /></b-navbar-brand>

      <b-collapse is-nav id="nav_collapse">

        <ul class="navbar-nav ml-auto">
          <li class="nav-item"><a href="#details" class="nav-link" v-smooth-scroll="{ offset: -140 }">Details</a></li>
          <li class="nav-item"><a href="#accessibility" class="nav-link" v-smooth-scroll="{ offset: -140 }">Accessibility</a></li>
          <li class="nav-item"><a href="#sponsors" class="nav-link" v-smooth-scroll="{ offset: -140 }">Sponsors</a></li>
          <li class="nav-item"><a href="#contact" class="nav-link" v-smooth-scroll="{ offset: -140 }">Contact</a></li>
        </ul>

      </b-collapse>

      <b-nav-toggle target="nav_collapse"></b-nav-toggle>

    </b-container>
  </b-navbar>
</template>
