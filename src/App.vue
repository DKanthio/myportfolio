<template>
  <div id="app">
  <div class="header-placeholder"></div>
    <Entete />
  <div class="main-content">
      <router-view />
  </div>
    <Footer />
  <div class="footer-placeholder"></div>
  </div>
</template>

<script>
import Entete from './components/Entete.vue';
import Footer from './components/Footer.vue';

export default {
  name: "App",
  components: {
    Entete,
    Footer
  }
};
</script>

<style scoped>
/* Vos styles pour App.vue */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


.footer {
  padding-bottom: 30px;
}



#app {
 
  display: flex;
  flex-direction: column;
  width: 200%;
  
}

.main-content {
  min-height: 100%;
  background-color:  #14051E;
  position: relative;
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 0px;
}


</style>
