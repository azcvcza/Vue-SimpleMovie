<template>
    <div id="app">
    <section class="hero is-primary is-medium">
      <router-view></router-view>

      <div class="hero-foot">
        <div class="columns is-mobile">
          <div v-for="movieChoice in movieChoices" class="column">
            <router-link :to="`/${movieChoice.id}`" tag="li" class="movie-choice">
              <i :class="[{ 'fa fa-check-circle favorite-check': movieChoice.favorite }]" aria-hidden="true"></i>
              <img :src="`${movieChoice.smallImgSrc}`" class="desktop"/>
              <p class="mobile movie-title">{{ movieChoice.subtitle }}</p>
            </router-link>
          </div>
        </div>
      </div>
    </section>
    
   
    
  </div>
</template>

<script>
const movies = {
  "dunkirk": {
    "id": 'dunkirk',
    "title": "Dunkirk",
    "subtitle": "Dunkirk",
    "description": `Miraculous evacuation of Allied soldiers from Belgium, Britain, Canada, and France, who were cut off and surrounded by the German army from the beaches and harbor of Dunkirk, France, during the Battle of France in World War II.`,
    "largeImgSrc": `url('https://image.tmdb.org/t/p/w780/fudEG1VUWuOqleXv6NwCExK0VLy.jpg')`,
    "smallImgSrc": 'https://image.tmdb.org/t/p/w185/fudEG1VUWuOqleXv6NwCExK0VLy.jpg',
    "releaseDate": 'July 21 2017',
    "duration": '1hr 46min',
    "genre": 'Action, Drama, History',
    "trailerPath": 'https://www.youtube.com/embed/F-eMt3SrfFU',
    "favorite": false
  },
  "interstellar": {
    "id": 'interstellar',
    "title": "Interstellar",
    "subtitle": "Interstellar",
    "description": `Interstellar chronicles the adventures of a group of explorers who make use of a newly discovered wormhole to surpass the limitations on human space travel and conquer the vast distances involved in an interstellar voyage.`,
    "largeImgSrc": `url('https://image.tmdb.org/t/p/w780/xu9zaAevzQ5nnrsXN6JcahLnG4i.jpg')`,
    "smallImgSrc": 'https://image.tmdb.org/t/p/w185/xu9zaAevzQ5nnrsXN6JcahLnG4i.jpg',
    "releaseDate": 'November 7 2014',
    "duration": '2hr 49min',
    "genre": 'Adventure, Drama',
    "trailerPath": 'https://www.youtube.com/embed/zSWdZVtXT7E',
    "favorite": false
  },
  "the-dark-knight-rises": {
    "id": 'the-dark-knight-rises',
    "title": "The Dark Knight Rises",
    "subtitle": "TDKR",
    "description": `Batman encounters the mysterious Selina Kyle and the villainous Bane, a new terrorist leader who overwhelms Gotham's finest. The Dark Knight resurfaces to protect a city that has branded him an enemy.`,
    "smallImgSrc": 'https://image.tmdb.org/t/p/w185/3bgtUfKQKNi3nJsAB5URpP2wdRt.jpg',
    "largeImgSrc": `url('https://image.tmdb.org/t/p/w780/3bgtUfKQKNi3nJsAB5URpP2wdRt.jpg')`,
    "releaseDate": 'July 20 2012',
    "duration": '2hr 44min',
    "genre": 'Action, Thriller',
    "trailerPath": 'https://www.youtube.com/embed/g8evyE9TuYk',
    "favorite": false
  },
  "inception": {
    "id": 'inception',
    "title": "Inception",
    "subtitle": "Inception",
    "description": `Cobb, a skilled thief is offered a chance to regain his old life as payment for a task considered to be impossible: \"inception\", the implantation of another person's idea into a target's subconscious.`,
    "smallImgSrc": 'https://image.tmdb.org/t/p/w185/s2bT29y0ngXxxu2IA8AOzzXTRhd.jpg',
    "largeImgSrc": `url('https://image.tmdb.org/t/p/w780/s2bT29y0ngXxxu2IA8AOzzXTRhd.jpg')`,
    "releaseDate": 'July 10 2010',
    "duration": '2hr 28min',
    "genre": 'Action, Adventure, Sci-Fi',
    "trailerPath": 'https://www.youtube.com/embed/8hP9D6kZseM',
    "favorite": false
  },
  "the-prestige": {
    "id": 'the-prestige',
    "title": "The Prestige",
    "subtitle": "Prestige",
    "description": `A mysterious story of two magicians whose intense rivalry leads them on a life-long battle for supremacy - to create the ultimate illusion whilst sacrificing everything they have to outwit the other.`,
    "smallImgSrc": 'https://image.tmdb.org/t/p/w185/c5o7FN2vzI7xlU6IF1y64mgcH9E.jpg',
    "largeImgSrc": `url('https://image.tmdb.org/t/p/w780/c5o7FN2vzI7xlU6IF1y64mgcH9E.jpg')`,
    "releaseDate": 'October 20 2006',
    "duration": '2hr 10min',
    "genre": 'Drama, Mystery, Sci-Fi',
    "trailerPath": 'https://www.youtube.com/embed/ijXruSzfGEc',
    "favorite": false
  }
}
export default {
  name: 'App',
  data () {
    return {
      movieChoices: movies
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
