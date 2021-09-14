<template>
  <v-app-bar app color="white" height="70">
    <v-container class="d-flex justify-space-between align-center">
      <div style="height: 70px;">
        <img src="../assets/eas.png" height="70" alt="Everything About Study">
      </div>
      <div class="menus">
        <v-btn text active-class="active__nav" tile v-for="(nav, n) in menus" :key="n" :to="nav.to">
          <span>{{ nav.title }}</span>
        </v-btn>
      </div>
    </v-container>  
  </v-app-bar>  
</template>

<script>
export default {
  data: () => ({
    menus: [
      { title: 'Home', icon: 'mdi-home', to: '/' },
      { title: 'Services', icon: 'mdi-cog', to: '/services' },
      { title: 'Blog', icon: 'mdi-post', to: '/blog' },
      { title: 'About Us', icon: 'mdi-account-box', to: '/about' },
      { title: 'Contact Us', icon: 'mdi-account-box', to: '/contact' }
    ]
  })
}
</script>

<style>
.menus .theme--light.v-btn--active:hover::before, .nav .theme--light.v-btn--active::before { opacity: 0 !important; }
.menus .v-btn { height: 70px !important; }
.active__nav {
  border-bottom: 3px solid #4a4dc7;
  color: #4a4dc7 !important;
  font-weight: 500 !important;
}
</style>