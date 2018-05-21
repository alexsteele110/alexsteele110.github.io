<template>
  <section class="section-stories" id="about">
      <div class="bg-video">
        <video class="bg-video__content" autoplay muted loop>
          <source src="../img/video.mp4" type="video/mp4">
          <source src="../img/video.webm" type="video/webm">
            Your browser is not supported!
        </video>
      </div>
      <div class="u-center-text u-margin-bottom-big">
        <h2 class="heading-secondary">
          About Me
        </h2>
      </div>

      <div class="row">
        <div class="story">
          <figure class="story__shape">
            <img src="../img/me.jpg" alt="Person on a tour" class="story__img">
            <figcaption class="story__caption">
              Alex Steele
            </figcaption>
          </figure>
          <div class="story__text">
            <h3 class="heading-tertiary u-margin-bottom-mini">{{ content.title }}</h3>
            <p class="paragraph" v-for="paragraph in content.paragraphs" :key="paragraph">
              {{ paragraph }}
            </p>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
export default {
  name: 'AboutMe',
  data() {
    return {
      content: {
        title: 'My Journey Into Software Development',
        paragraphs: [
          'First paragraph',
          'Second paragraph'
        ]
      }    
    };
  }
};
</script>

<style lang="css">
</style>
