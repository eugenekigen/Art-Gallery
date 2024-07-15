<template>
 <v-app style="background-image: url('Student Wallpaper.png'); background-size:cover; background-position:center">
  <v-container class="d-flex justify-center align-center min-vh-100">
  <v-card max-width="500" width="100%" elevation="0" class="login-card mt-16" color="transparent">
  <v-img src="Art_Gallery_Studio_Logo.png" alt="logo" height="200"></v-img>
   <v-row>
    <v-col>
     <v-form>
      <v-text-field label="First Name" variant="outlined" prepend-inner-icon="mdi-account" style="color:white"></v-text-field>
      <v-text-field label="Last Name" variant="outlined" prepend-inner-icon="mdi-account" style="color:white" ></v-text-field>
      <v-select label="Gender" 
      style="color:white"
      variant="outlined" 
      prepend-inner-icon="mdi-gender-male-female"
      :items="['Male', 'Female']"
      
      
      ></v-select>
      <v-text-field label="Email" variant="outlined" prepend-inner-icon="mdi-email" style="color:white"></v-text-field>
      <v-text-field label="Password" variant="outlined" prepend-inner-icon="mdi-lock" style="color:white"></v-text-field>
      
     
      <v-btn type="submit" width="100%" color="white" style="text-transform: capitalize;" to="/register" rounded elevation="10"><v-icon>mdi-account-plus</v-icon> Register</v-btn>

     </v-form>


    </v-col>
   </v-row>
   </v-card>
  </v-container>

 </v-app>
</template>

<script>
export default{
    data(){
       return{
           gender:null,
        }
    }
}        

</script>