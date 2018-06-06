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
          <img :src="content.image" alt="About me" class="story__img">
          <figcaption class="story__caption">
            {{ content.name }}
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
        name: 'Alex Steele',
        image: '../static/me.jpg',
        title: 'My Journey in Software Development',
        paragraphs: [
          'Not so long ago I made a decision to learn how to program and from there quickly realized it was something I loved to do. I currently specialize in web development and I strive to learn and work with all aspects involved in building interesting web applications.',
          'I enjoy utilizing the power of frameworks like React to make complex, performant, and modern software. Node is another preference of mine in order to keep most of my workflow inside JavaScript. I like to keep my front end design clean and simple, whether that be from creating custom CSS and Sass for this portfolio, or borrowing from the excellent CSS libraries offered today like Bootstrap or Material UI.'
        ]
      }    
    };
  }
};
</script>

<style lang="css">
</style>
