<template>
 <v-app style="background-image: url('Original Wallpaper.jpg'); background-size:cover; background-position:center">
  <v-container fluid fill-height>
         <v-img src="Art_Gallery_Studio_Logo.png" alt="logo" height="400"></v-img>

    <v-row justify="center" align="center" class="ma.0" >
      <v-col cols="12" sm="8" md="6" lg="4">
        <v-card class="pa-8" elevation="0" color="transparent" style="margin-top:253px">
           <v-row class="my-6">
             <v-col>
                <v-btn width="100%" color="orange" style="text-transform:capitalize ;"  elevation="0" to="/register" rounded>
                <v-icon>mdi-account-plus</v-icon> Get Started
              </v-btn>
             </v-col> 
             <v-col>
                 <v-btn width="100%" color="orange" style="text-transform:capitalize;"  elevation="0" rounded to="/login">   
                 <v-icon>mdi-login</v-icon> Login
                 </v-btn>
             </v-col>
            </v-row>
          </v-card>  
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>