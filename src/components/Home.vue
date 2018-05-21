<template>
  <div>

    <Header></Header>

    <section class="section-about" id="projects">
      <div class="u-center-text u-margin-bottom-big">
        <h2 class="heading-secondary">
          My projects
        </h2>
      </div>

      <div class="row">
        <div class="col-1-of-3" v-for="data in cardData" :key="data.title">
          <Card :message="data.message" :title="data.title" :image="data.image" :url="data.url"></Card>
        </div>
      </div>
    </section>

    <main>

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
              <h3 class="heading-tertiary u-margin-bottom-mini">My Journey Into Software Development</h3>
              <p class="paragraph">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </p>
              <p class="paragraph">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </p>
            </div>
          </div>
        </div>
      </section>

      <div class="u-center-text">
        <h2 class="heading-secondary u-margin-top-huge">
          Skills
        </h2>
      </div>

      <section class="gallery" id="skills">
        <figure class="gallery__item" v-for="data in galleryData" :key="data.text">
          <img :src="data.image" :alt="data.text" class="gallery__img">
        </figure>       
      </section>

    </main>

    <footer class="footer">
      <div class="row">
        2018, Alexander Steele
      </div>
    </footer>

  </div>
</template>

<script>
import Header from './Header';
import Card from './Card';

export default {
  name: 'Home',
  components: {
    Header,
    Card
  },
  data() {
    return {
      cardData: [
        {
          title: 'Wanderful',
          message:
            'A travel roulette web app. Go to random locations throughout the world to get restaurant, flight, and hotel information.',
          image: '../static/wanderful.png',
          url: 'http://www.wanderful-travel.com'
        },
        {
          title: 'BeerMe',
          message:
            'A hub for beer enthusiasts. Come here to search, review, and find community ratings and comments on thousands of beers.',
          image: '../static/beerme.png',
          url: 'https://vast-retreat-88379.herokuapp.com/'
        },
        {
          title: 'Card Title Number Three',
          message:
            'Testing 2 Lorem ipsum dolor sit amet, ex sonet suavitate mei. Nec ut errem munere. Ne cum ubique ceteros. His vidit tollit eirmod cu.',
          image: '../static/nat-7.jpg',
          url: 'https://google.com'
        }
      ],
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
