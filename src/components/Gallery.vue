<template>
    <section id="skills">
        <div class="u-center-text">
            <h2 class="heading-secondary u-margin-top-huge">
                Skills
            </h2>
        </div>
        <div class="gallery">
            <figure class="gallery__item" v-for="data in galleryData" :key="data.text">
                <span class="gallery__text" style="position:absolute;">{{ data.text }}</span>
                <img :src="data.image" :alt="data.text" class="gallery__img">
            </figure>        
        </div>
    </section>
</template>

<script>
export default {
  name: 'Gallery',
  data() {
    return {
      galleryData: [
        {
          image: '../static/js.jpg',
          text: 'JavaScript'
        },
        {
          image: '../static/node.png',
          text: 'NodeJS'
        },
        {
          image: '../static/react.png',
          text: 'React'
        },
        {
          image: '../static/vue.png',
          text: 'VueJS'
        },
        {
          image: '../static/mongodb.png',
          text: 'MongoDB'
        },
        {
          image: '../static/sass.png',
          text: 'Sass'
        },
        {
          image: '../static/python.png',
          text: 'Python'
        },
        {
          image: '../static/d3.png',
          text: 'D3.js'
        }
      ]
    };
  }
};
</script>

<style lang="css">
</style>
