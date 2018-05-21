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
      <a v-if="githubUrl":href="githubUrl" class="btn-card" target="_blank">GitHub</a>
      <a v-if="liveUrl" :href="liveUrl" class="btn-card" target="_blank">Live site</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: ['message', 'title', 'image', 'liveUrl', 'githubUrl']
};
</script>

<style lang="css">
</style>
