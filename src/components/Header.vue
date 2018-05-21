<template lang="html">
  <header class="header">
    <Navigation></Navigation>
    <div class="header__text-box">
      <h1 class="heading-primary">
        <span class="heading-primary--main">Alex Steele</span>
        <span class="heading-primary--sub">web developer</span>
      </h1>
      <div class="header__seenon-text">Contact Me</div>
      <div class="header__seenon-logos">
        <div v-for="data in navData">
          <a :href="data.url">
            <svg>
              <use :xlink:href="data.icon"></use>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import Navigation from './Navigation';

export default {
  name: 'Header',
  components: {
    Navigation
  },
  data() {
    return {
      navData: [
        {
          icon: '../static/sprite.svg#icon-github-with-circle',
          url: 'https://github.com/alexsteele110'
        },
        {
          icon: '../static/sprite.svg#icon-mail',
          url: 'mailto:alexsteele110@gmail.com'
        },
        {
          icon: '../static/sprite.svg#icon-linkedin-with-circle',
          url: 'https://linkedin.com/in/asteele110'
        }    
        
      ]
    };
  }
};
</script>

<style lang="css">
</style>
