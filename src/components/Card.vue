<template lang="html">
  <div class="card">
    <div class="card__media">
      <img :src="image" alt="card media">
    </div>
    <div class="card__content">
      <h3 class="heading-tertiary u-margin-bottom-mini">{{ title }}</h3>
      <p class="paragraph">{{ message }}</p>
    </div>
    <div class="card__footer">
      <a href="#section-about" class="btn-card">Live site</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: ['message', 'title', 'image']
};
</script>

<style lang="css">
</style>
