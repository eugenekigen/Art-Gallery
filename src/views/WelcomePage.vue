<template>
<v-app style="background-image: url('Illustration 3.png'); background-position:center;">
  <v-container fluid fill-height class="d-flex align-center justify-center">
    <v-row>
      <v-col cols="12" md="8" lg="6">
        <v-card class="pa-4" elevation="10">
          <v-card-title class="headline text-center">
            <v-icon large>mdi-palette</v-icon>
            <span class="ml-2">Welcome to Art Gallery</span>
          </v-card-title>
          <v-card-subtitle class="text-center mb-4">
            <p>Immerse yourself in creativity</p>
          </v-card-subtitle>
          <v-card-text>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <p class="text-center">
                    Discover a world of art, explore exhibitions, and get inspired by our collection of masterpieces.
                    We invite you to browse through our gallery, view artists' works, and enjoy the beauty of art.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-card-text>
          <v-divider></v-divider>
          <v-card-actions class="justify-center">
            <v-btn to="/gallery" color="primary" large class="mt-4">Explore Gallery</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'Welcome'
};
</script>

<style scoped>
.v-container {
  background-image: url('public/abstract-smooth-orange-background-layout-design-studio-room-web-template-business-report-with-smooth-circle-gradient-color.jpg'); /* Add your background image here */
  background-size: cover;
  background-position: center;
}

.ml-2 {
  margin-left: 8px;
}

.text-center {
  text-align: center;
}

.v-card {
  background: rgba(255, 255, 255, 0.9); /* Semi-transparent background for card */
}

.v-card-title {
  color: #3f51b5; /* Primary color */
}

.v-card-subtitle p {
  font-size: 1.2em;
  color: #3f51b5; /* Primary color */
}

.v-card-text {
  font-size: 1em;
  color: #333; /* Dark text color */
}

.v-btn {
  text-transform: capitalize; /* Preserve button text case */
}

.v-divider {
  margin: 16px 0;
}
</style>
