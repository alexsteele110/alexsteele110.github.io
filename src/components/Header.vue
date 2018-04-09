<template lang="html">
  <header class="header">
    <Navigation></Navigation>
    <div class="header__text-box">
      <h1 class="heading-primary">
        <span class="heading-primary--main">Alex Steele</span>
        <span class="heading-primary--sub">web developer</span>
      </h1>
      <div class="header__seenon-text">Contact</div>
      <div class="header__seenon-logos">
        <a>
          <img src="../img/GitHub-Mark-Light-32px.png" alt="">
        </a>
        <a>
          <img src="../img/In-White-28px-TM.png" alt="">
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
  }
};
</script>

<style lang="css">
</style>
