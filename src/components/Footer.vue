<template>
  <footer class="footer">
      <div class="row">
        <span class="paragraph">&copy;{{ content.year }}, {{ content.name }}</span><br>
        <span class="paragraph">{{ content.subtitle }}</span><br>
        <img :src="content.image" alt="Vue" height="32" width="32" />
      </div>
    </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      content: {
        name: 'Alexander Steele',
        image: '../static/vue.png',
        year: 2018,
        subtitle: 'Made with Vue.js'
      }    
    };
  }
};
</script>

<style lang="css">
</style>
