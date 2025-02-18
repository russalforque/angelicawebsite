<template>
  <header>
    <NavBar></NavBar>
  </header>
  <footer>
    <SiteFooter></SiteFooter>
  </footer>
</template>

<script>
import NavBar from './components/NavBar.vue';
import SiteFooter from './components/SiteFooter.vue';

export default {
  components:{
    NavBar,
    SiteFooter
  }
}
</script>

<style scoped>
  
</style>
