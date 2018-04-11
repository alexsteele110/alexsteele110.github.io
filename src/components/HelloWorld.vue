<template>
  <div>

    <Header></Header>

    <section class="section-about" id="portfolio">
      <div class="u-center-text u-margin-bottom-big">
        <h2 class="heading-secondary">
          My projects
        </h2>
      </div>

      <div class="row">
        <div class="col-1-of-3" v-for="data in cardData">
          <Card :message="data.message" :title="data.title" :image="data.image"></Card>
        </div>
      </div>
    </section>

    <main>

      <section class="section-stories">
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

      <section class="gallery">
        <figure class="gallery__item" v-for="data in galleryData">
          <img :src="data.image" :alt="data.text" class="gallery__img">
        </figure>
      </section>

    </main>

    <footer class="footer">
      <div class="footer__logo-box">

        <picture class="footer__logo">
          <source srcset="../img/logo-green-small-1x.png 1x, ../img/logo-green-small-2x.png 2x"
                  media="(max-width: 37.5rem)">
          <img srcset="../img/logo-green-1x.png 1x, ../img/logo-green-2x.png 2x" alt="Full logo" src="../img/logo-green-2x.png">
        </picture>


      </div>
      <div class="row">
        <div class="col-1-of-2">
          <div class="footer__navigation">
            <ul class="footer__list">
              <li class="footer__item"><a href="#" class="footer__link">Company</a></li>
              <li class="footer__item"><a href="#" class="footer__link">Contact us</a></li>
              <li class="footer__item"><a href="#" class="footer__link">Careers</a></li>
              <li class="footer__item"><a href="#" class="footer__link">Privacy</a></li>
              <li class="footer__item"><a href="#" class="footer__link">Terms</a></li>
            </ul>
          </div>
        </div>
        <div class="col-1-of-2">
          <p class="footer__copyright">
            Built by <a href="#" class="footer__link">Jonas Schmedtmann</a> for my online course <a href="" class="footer__link">Advanced CSS and Sass</a>. Copyright &copy; by Jonas Schmedtmann. You are 100% allowed to use this webpage for both personal and commercial use, but NOT to claim it as your own design. A credit to the original author, Jonas Schmedtmann, is of course highly appreciated!
          </p>
        </div>
      </div>
    </footer>

  </div>
</template>

<script>
import Header from './Header';
import Card from './Card';

export default {
  name: 'HelloWorld',
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
          image: '../static/nat-8.jpg'
        },
        {
          title: 'BeerMe',
          message:
            'A hub for beer enthusiasts. Come here to search, review, and see community ratings and comments on thousands of beers.',
          image: '../static/nat-9.jpg'
        },
        {
          title: 'Card Title Number Three',
          message:
            'Testing 2 Lorem ipsum dolor sit amet, ex sonet suavitate mei. Nec ut errem munere. Ne cum ubique ceteros. His vidit tollit eirmod cu.',
          image: '../static/nat-7.jpg'
        }
      ],
      galleryData: [
        {
          image: '../static/react.png',
          text: 'React'
        },
        {
          image: '../static/js.jpg',
          text: 'JavaScript'
        },
        {
          image: '../static/node.png',
          text: 'NodeJS'
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
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
