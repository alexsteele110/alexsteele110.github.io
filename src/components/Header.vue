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
        <a v-for="icon in icons">
          <svg>
            <use :xlink:href="icon"></use>
          </svg>
        </a>
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
      icons: [
        '../static/sprite.svg#icon-github-with-circle',
        '../static/sprite.svg#icon-mail',
        '../static/sprite.svg#icon-linkedin-with-circle'
      ]
    };
  }
};
</script>

<style lang="css">
</style>
