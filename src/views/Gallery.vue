<template>
  <v-container fluid fill-height class="d-flex align-center justify-center">
    <v-row>
      <v-col v-for="movie in movies" :key="movie.id" cols="12" sm="6" md="4">
        <v-card class="mx-auto" max-width="344" @click="goToTrailer(movie.id)">
          <v-img :src="movie.image" height="200px" cover>
            <v-row align="end" class="fill-height">
              <v-col class="d-flex justify-center">
                <v-btn @click.stop="goToTrailer(movie.id)" icon>
                </v-btn>
              </v-col>
            </v-row>
          </v-img>
          <v-card-title>{{ movie.title }}</v-card-title>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'MovieList',
  data() {
    return {
      movies: [
        { id: 1, title: 'Drawings', image: 'public/Pencil Drawing.jpg' },
        { id: 2, title: 'Coloured Pencils', image: 'public/Coloured Pencil 2.jpg' },
        { id: 3, title: 'Paintings', image: 'public/Painting 3.jfif' },
        { id: 4, title: 'Illustrations', image: 'public/11_illustration.jpg' },
        { id: 5, title: 'Vector Art Design', image: 'public/Vector Graphic Design.jpg' },
        { id: 6, title: 'Logo Design', image: 'public/Logo Design.jfif' },

        // Add more movie objects here
      ]
    };
  },
  methods: {
    goToTrailer(id) {
      this.$router.push({ name: 'MovieTrailer', params: { id } });
    }
  }
};
</script>

<style scoped>
.v-img {
  position: relative;
}

.v-card-title {
  font-weight: bold;
}

.v-btn {
  background: rgba(0, 0, 0, 0.5);
  color: white;
}

.v-btn:hover {
  background: rgba(0, 0, 0, 0.7);
}
</style>