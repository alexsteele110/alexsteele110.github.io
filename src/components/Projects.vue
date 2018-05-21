<template>
    <section class="section-about" id="projects">
        <div class="u-center-text u-margin-bottom-big">
            <h2 class="heading-secondary">My projects</h2>
        </div>
        <div class="row">
            <div class="col-1-of-3" v-for="data in cardData" :key="data.title">
                <Card 
                :message="data.message" 
                :title="data.title" 
                :image="data.image" 
                :url="data.url">
                </Card>
            </div>
        </div>
    </section>
</template>

<script>
import Card from './Card';

export default {
  name: 'Projects',
  components: {
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
      ]
    };
  }
};
</script>

<style lang="css">
</style>
