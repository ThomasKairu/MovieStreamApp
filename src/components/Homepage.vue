<template>
    <v-container fluid>
        <v-row>
            <v-col>
                <v-img src="./../../public/movieapp.jpg" 
                    >
                    <v-container fill-height fluid class="hero-overlay">
                        <v-row align="center" justify="center">
                            <v-col class="text-center">
                                <h1 class="display-2 white--text mb-4">Discover Endless Entertainment</h1>
                                <p class="subheading white--text">Explore a vast collection of movies, music, and TV shows.
                                </p>
                                <v-btn color="red" dark large @click="explore">Explore Now</v-btn>
                            </v-col>
                        </v-row>
                    </v-container>
                </v-img>
            </v-col>
        </v-row>

        <v-row>
            <v-col>
                <h2 class="headline">Featured Movies</h2>
                <template>
  <v-row>
    <v-col
      v-for="n in 9"
      :key="n"
      class="d-flex child-flex"
      cols="4"
    >
      <v-img
        :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
        :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
        aspect-ratio="1"
        cover
        class="bg-grey-lighten-2"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey-lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
    </v-col>
  </v-row>
</template>
            </v-col>
        </v-row>

        <!-- Trending Section -->
        <v-row>
            <v-col>
                <h2 class="headline">Trending Now</h2>
                <!-- Display a carousel or grid of trending content -->
            </v-col>
        </v-row>

        <!-- Recently Added Section -->
        <v-row>
            <v-col>
                <h2 class="headline">Recently Added</h2>
                <!-- Display a carousel or grid of recently added content -->
            </v-col>
        </v-row>
    </v-container>
</template>
  
<script>
export default {
    name: 'Home',
    methods: {
        explore() {
            // Implement navigation or any other action when the "Explore Now" button is clicked
        },
    },
};
</script>
  
