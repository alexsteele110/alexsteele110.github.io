<template>
    <section id="skills">
        <div class="u-center-text">
            <h2 class="heading-secondary u-margin-top-huge">
                Skills
            </h2>
        </div>
        <div class="gallery">
            <figure class="gallery__item" v-for="data in galleryData" :key="data.text">
                <span class="gallery__text" :style="{ color: data.textColor }">{{ data.text }}</span>
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
          text: 'JavaScript',
          textColor: '#222222'
        },
        {
          image: '../static/node.png',
          text: 'NodeJS',
          textColor: '#ccc'
        },
        {
          image: '../static/react.png',
          text: 'React',
          textColor: '#ccc'
        },
        {
          image: '../static/vue.png',
          text: 'VueJS',
          textColor: '#ccc'
        },
        {
          image: '../static/mongodb.png',
          text: 'MongoDB',
          textColor: '#222222'
        },
        {
          image: '../static/sass.png',
          text: 'Sass',
          textColor: '#222222'
        },
        {
          image: '../static/python.png',
          text: 'Python',
          textColor: '#ccc'
        },
        {
          image: '../static/d3.png',
          text: 'D3.js',
          textColor: '#ccc'
        }
      ]
    };
  }
};
</script>

<style lang="css">
</style>
