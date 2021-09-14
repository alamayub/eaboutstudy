<template>
  <v-app>
    <Navbar />
    <v-main>
      <router-view/>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Navbar from './components/Navbar'
import Footer from './components/Footer'
export default {
  name: 'App',
  components: { Navbar, Footer },
};
</script>

<style>
html { scroll-behavior: smooth; }
/* Container */
.container {
  max-width: 1250px !important;
  margin-right: auto !important;
  margin-left: auto !important;
  padding: 12px !important;
}
/* Button */
.v-btn {
  text-transform: capitalize !important;
  font-weight: 400 !important;
  font-size: 12px !important;
}

/* Image */
img {
  height: 100%;
  width: 100%;
  display: block;
  object-fit: cover;
}

/* Inputs */
.v-input input, .v-input textarea { 
  font-size: 13px !important; 
  letter-spacing: .75px !important; 
}
.v-input .v-label { 
  font-size: 13px !important; 
  letter-spacing: 1px !important; 
}
.v-input__icon .v-icon.v-icon, .v-select-list .v-icon.v-icon { font-size: 16px !important; }
.v-text-field--outlined.v-input--is-focused fieldset { border: 1px solid #4a4dc7  !important; }
.v-text-field--outlined.v-input--has-state fieldset { border: 1px solid #f36c27 !important; }
</style>