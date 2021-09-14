<template>
  <v-footer color="white" class="py-6 py-sm-8 py-md-10 py-lg-12 elevation-6" padless>
    <v-container class="footer">
      <div class="company">
        <div style="height: 100px;">
          <img src="../assets/eas.png" style="max-width: 300px;" height="100" alt="Everything About Study">
        </div>   
        <div class="mt-3 para">Top instructor from around the world teach millions of student.</div>
      </div>
      <div class="footer__links">
        <div class="links">
          <div class="link__title">Information</div>
          <div class="para" v-for="(inf, i) in info" :key="i">{{ inf }}</div>
        </div>
        <div class="links">
          <div class="link__title">Links</div>
          <div class="para" v-for="(link, l) in links" :key="l">{{ link }}</div>
        </div>
        <div class="links">
          <div class="link__title">Services</div>
          <div class="para" v-for="(service, s) in services" :key="s">{{ service }}</div>
        </div>
        <div class="links">
          <div class="link__title">Contact</div>
          <div class="para" v-for="(con, c) in contact" :key="c">{{ con }}</div>
          <div class="socials"> 
            <v-btn icon small v-for="(social, s) in socials" :key="s" color="secondary" target="_blank" :href="social.to">
              <v-icon size="14" v-text="social.icon" />
            </v-btn>  
          </div>
        </div>  
      </div>
    </v-container>  
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    info: ['Home', 'About', 'Courses', 'Blog'],
    links: ['Student', 'Business', 'Instructor'],
    services: ['Design', 'Study', 'Business', 'UI/UX'],
    contact: ['24th street, downtown, New York', 'info@e-learn.com', '(545) 555-0214'],
    socials: [
      { icon: 'mdi-facebook', to: 'https://www.facebook.com' },
      { icon: 'mdi-twitter', to: 'https://www.twitter.com' },
      { icon: 'mdi-youtube', to: 'https://www.youtube.com' },
      { icon: 'mdi-linkedin', to: 'https://www.linkedin.com' }  
    ]
  })  
}
</script>

<style scoped>
.footer {
  display: grid;
  grid-template-columns: 280px calc(100% - 330px);
  grid-gap: 50px;  
}
.footer__links {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(25%, 1fr));  
}
.para {
  color: grey; 
  font-size: 13px; 
}
.links .para { margin-bottom: 8px; }
.links .para:last-child { margin-bottom: 0 !important; }
.link__title {
  font-weight: bold;
  margin-bottom: 16px;  
  letter-spacing: .5px;
  font-size: 17px;
}
@media (max-width: 960px) {
  .footer { grid-gap: 40px; }  
  .footer__links { grid-template-columns: repeat(auto-fit, minmax(50%, 1fr)); }  
}
@media (max-width: 600px) {
  .footer { grid-template-columns: repeat(auto-fit, minmax(100%, 1fr)); grid-gap: 30px;  }  
  .footer__links { row-gap: 20px; }
}
</style>