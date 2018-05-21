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
                :liveUrl="data.liveUrl"
                :githubUrl="data.githubUrl">
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
          liveUrl: 'http://www.wanderful-travel.com',
          githubUrl: 'https://github.com/alexsteele110/Voyage2-Bears-11'
        },
        {
          title: 'BeerMe',
          message:
            'A hub for beer enthusiasts. Come here to search, review, and find community ratings and comments on thousands of beers.',
          image: '../static/beerme.png',
          liveUrl: 'https://vast-retreat-88379.herokuapp.com/',
          githubUrl: 'https://github.com/alexsteele110/BeerMe'
        },
        {
          title: 'HTML/Image Exporter',
          message:
            'Combines the power of Node and puppeteer to grab HTML, images, and screenshots of web pages into a single zip file.',
          image: '../static/exporter.png',
          githubUrl: 'https://github.com/alexsteele110/cms-exporter'
        }
      ]
    };
  }
};
</script>

<style lang="css">
</style>
