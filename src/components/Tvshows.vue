<template>
    <v-container>

      <v-row>
        <v-col>
          <v-img
            src="./../../public/explore.jpg" 
          >
            <v-container fill-height fluid class="tvshows-header-overlay">
              <v-row align="center" justify="center">
                <v-col class="text-center">
                  <h1 class="display-2 white--text mb-4">Explore Exciting TV Shows</h1>
                  <p class="subheading white--text">Discover a variety of TV shows across different genres.</p>
                  <v-btn color="red" dark large @click="exploreTVShows">Explore TV Shows</v-btn>
                </v-col>
              </v-row>
            </v-container>
          </v-img>
        </v-col>
      </v-row>
  

      <v-row>
        <v-col>
          <h2 class="headline">Featured TV Shows</h2>
          <v-carousel>
            
            <v-carousel-item v-for="(show, index) in featuredTVShows" :key="index">
              <v-img :src="show.imageUrl" aspect-ratio="16/9"></v-img>
              <v-carousel-item-title>{{ show.title }}</v-carousel-item-title>
            </v-carousel-item>
          </v-carousel>
        </v-col>
      </v-row>
  

      <v-row>
        <v-col>
          <h2 class="headline">Popular Genres</h2>
          <v-row>
            
            <v-col v-for="(genre, index) in popularGenres" :key="index" cols="12" md="4">
              <v-card>
                <v-img :src="genre.imageUrl" aspect-ratio="16/9"></v-img>
                <v-card-title>{{ genre.name }}</v-card-title>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
  
      
      <v-row>
        <v-col>
          <h2 class="headline">New Releases</h2>
          <v-carousel>
            
            <v-carousel-item v-for="(release, index) in newReleases" :key="index">
              <v-img :src="release.imageUrl" aspect-ratio="16/9"></v-img>
              <v-carousel-item-title>{{ release.title }}</v-carousel-item-title>
            </v-carousel-item>
          </v-carousel>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'TVShows',
    data: () => ({
      featuredTVShows: [
        { title: 'TV Show 1', imageUrl: 'https://img.youtube.com/vi/ZTFDjaduHtY/maxresdefault.jpg' },
        { title: 'TV Show 2', imageUrl: 'https://img.youtube.com/vi/T81vO3_UJ2g/maxresdefault.jpg' },
        // Add more featured TV shows
      ],
      popularGenres: [
        { name: 'Drama - American Nightmare season 1 (2024)', imageUrl: 'https://img.youtube.com/vi/7E-NoSq3QbY/mqdefault.jpg' },
        { name: 'Comedy - The Vince Staples Show (2024)', imageUrl: 'https://img.youtube.com/vi/xK-OvhrHCjw/mqdefault.jpg' },
        { name: 'Action - Griselda (2024)', imageUrl:'https://img.youtube.com/vi/rQNoO5JtkrI/mqdefault.jpg' },

        
      ],
      newReleases: [
        { title: 'Shogun', imageUrl: 'https://img.youtube.com/vi/yAN5uspO_hk/maxresdefault.jpg' },
        { title: 'Formular 1:Drive to survive', imageUrl: 'https://img.youtube.com/vi/wBu4apj0wv8/maxresdefault.jpg' },
        
      ],
    }),
    methods: {
      exploreTVShows() {
        // Implement navigation or any other action when the "Explore TV Shows" button is clicked
      },
    },
  };
  </script>