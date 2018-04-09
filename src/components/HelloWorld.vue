<template>
  <div>

    <Header class="u-margin-bottom-big"></Header>

    <section class="section-about" id="portfolio">
      <div class="u-center-text u-margin-bottom-big">
        <h2 class="heading-secondary">
          Portfolio of work
        </h2>
        <hr class="test">
      </div>

      <div class="row">
        <div class="col-1-of-3" v-for="data in cardData">
          <Card :message="data.message" :title="data.title" :image="data.image"></Card>
        </div>
      </div>
    </section>

    <main>

      <section class="section-stories u-margin-bottom-big">
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
              <img src="../img/nat-6.jpg" alt="Person on a tour" class="story__img">
              <figcaption class="story__caption">
                Alex Steele
              </figcaption>
            </figure>
            <div class="story__text">
              <h3 class="heading-tertiary u-margin-bottom-small">Wow! My life is completely different now</h3>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </p>
              <br />
              <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </p>
            </div>
          </div>
        </div>
      </section>

      <div class="u-center-text u-margin-bottom-medium">
        <h2 class="heading-secondary">
          Skills
        </h2>
      </div>

      <section class="gallery">
        <figure class="gallery__item">
          <img src="../img/react.png" alt="Gallery image 1" class="gallery__img">
        </figure>
        <figure class="gallery__item">
          <img src="../img/js.jpg" alt="Gallery image 2" class="gallery__img">
        </figure>
        <figure class="gallery__item">
          <img src="../img/sass.png" alt="Gallery image 3" class="gallery__img">
        </figure>
        <figure class="gallery__item">
          <img src="../img/node.png" alt="Gallery image 1" class="gallery__img">
        </figure>
        <figure class="gallery__item">
          <img src="../img/mongodb.png" alt="Gallery image 1" class="gallery__img">
        </figure>
        <figure class="gallery__item">
          <img src="../img/vue.png" alt="Gallery image 1" class="gallery__img">
        </figure>
        <figure class="gallery__item">
          <img src="../img/d3.png" alt="Gallery image 1" class="gallery__img">
        </figure>

      </section>

      <!-- <section class="section-book">
        <div class="row">
          <div class="book">
            <div class="book__form">
              <div class="u-margin-bottom-medium">
                <h2 class="heading-secondary">Start booking now</h2>
              </div>
              <form action="#" class="form">
                <div class="form__group">
                  <input type="text" class="form__input" placeholder="Full Name" id="name" required>
                  <label for="name" class="form__label">Full name</label>
                </div>
                <div class="form__group">
                  <input type="email" class="form__input" placeholder="Email address" id="email" required>
                  <label for="email" class="form__label">Email address</label>
                </div>

                <div class="form__group u-margin-bottom-medium">
                  <div class="form__radio-group">
                    <input type="radio" class="form__radio-input" id="small" name="size">
                    <label for="small" class="form__radio-label">
                      <span class="form__radio-button"></span>
                      Small tour group
                    </label>
                  </div>

                  <div class="form__radio-group">
                    <input type="radio" class="form__radio-input" id="large" name="size">
                    <label for="large" class="form__radio-label">
                      <span class="form__radio-button"></span>
                      Large tour group
                    </label>
                  </div>
                </div>

                <div class="form__group">
                  <button class="btn btn--green">Next step &rarr;</button>
                </div>
              </form>
            </div>
          </div>
        </div>
      </section> -->
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

    <!-- <div class="popup" id="popup">
      <div class="popup__content">
        <div class="popup__left">
          <img src="" alt="Tour photo" class="popup__img">
          <img src="" alt="Tour photo" class="popup__img">
        </div>
        <div class="popup__right">
          <a href="#section-tours" class="popup__close">&times;</a>
          <h2 class="heading-secondary u-margin-bottom-small">Start booking now</h2>
          <h3 class="heading-tertiary u-margin-bottom-small">Important &ndash; Please read these terms before booking</h3>
          <p class="popup__text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          </p>
          <a href="#" class="btn btn--green">Book now</a>
        </div>
      </div>
    </div> -->
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
            'Testing 2 Lorem ipsum dolor sit amet, ex sonet suavitate mei. Nec ut errem munere.',
          image: '../static/nat-8.jpg'
        },
        {
          title: 'BeerMe',
          message:
            'Testing 2 Lorem ipsum dolor sit amet, ex sonet suavitate mei. Nec ut errem munere. Ne cum ubique ceteros. His vidit tollit eirmod cu, doming accusamus posidonium id vim.',
          image: '../static/nat-9.jpg'
        },
        {
          title: 'Card Title Number Three',
          message:
            'Testing 2 Lorem ipsum dolor sit amet, ex sonet suavitate mei. Nec ut errem munere. Ne cum ubique ceteros. His vidit tollit eirmod cu.',
          image: '../static/nat-7.jpg'
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
