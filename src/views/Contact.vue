<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="6">
        <v-card>
          <v-card-title style="background-color: grey; color: white;" class="text-center">
            <v-icon>mdi-account-box</v-icon>
            <span class="ml-2">Contact Us</span>
          </v-card-title>
          <v-card-text>
            <v-form>
              <v-text-field
                v-model="name"
                label="Name"
                outlined
                variant="underlined"
                required
              ></v-text-field>
              <v-text-field
                v-model="email"
                label="Email"
                outlined
                variant="underlined"
                required
              ></v-text-field>
              <v-textarea
                v-model="message"
                label="Message"
                outlined
                variant="underlined"
                rows="5"
                required
              ></v-textarea>
              <v-btn @click="submitForm" color="grey" width="100%" style="text-transform: capitalize;">Submit</v-btn>
            </v-form>
          </v-card-text>
        </v-card>
      </v-col>

      <!-- Map Section -->
      <v-col cols="12" md="6">
        <v-card>
          <v-card-title style="background-color: grey; color: white;" class="text-center">
            <v-icon>mdi-map</v-icon>
            <span class="ml-2">Our Location</span>
          </v-card-title>
          <v-card-text>
            <!-- Replace the src with your desired map URL -->
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3153.5510492543757!2d-122.419418!3d37.774929!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8085808b8b8b8b8b%3A0x1b8b8b8b8b8b8b8b!2sSan%20Francisco%2C%20CA!5e0!3m2!1sen!2sus!4v1638287629301!5m2!1sen!2sus"
              width="100%"
              height="300"
              style="border:0;"
              allowfullscreen=""
              loading="lazy"
            ></iframe>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    };
  },
  methods: {
    submitForm() {
      // Handle form submission here
      alert('Form submitted!');
    }
  }
};
</script>

<style scoped>
.ml-2 {
  margin-left: 8px;
}
</style>

