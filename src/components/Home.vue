<template>
  <div>
    <Header></Header>
    <main>
      <Projects></Projects>
      <AboutMe></AboutMe>
      <Gallery></Gallery> 
    </main>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './Header';
import Footer from './Footer';
import Card from './Card';
import Projects from './Projects';
import AboutMe from './AboutMe';
import Gallery from './Gallery';

export default {
  name: 'Home',
  components: {
    Header,
    Footer,
    Card,
    Projects,
    AboutMe,
    Gallery
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
