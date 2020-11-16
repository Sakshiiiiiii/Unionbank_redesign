<template>
  <!--Your App Starts Here -->
  <v-app id="inspire">
    
    <!--Header -->
    <v-app-bar color="red" dark fixed app>
      
       <!-- Component Example -->
       <v-row class="hidden-sm-and-down">
<v-col sm="10">
  <UbiLogo/> 
</v-col> 
</v-row>
      <v-row class="hidden-sm-and-down">
          <!-- tab will be hidden in sm(i pad) and other small screen. It is only for mobile screen -->
          <GlobalNavigation/> 
        </v-row>
        <v-row class="hidden-md-and-up">
          <v-col sm="10">
  <UbiLogo/> 
</v-col> 
          <!-- <v-col sm="8"></v-col> -->
          <v-col sm="1" class="mb-sm-2 ma-sm-4 mb-2 ma-4 mx-0" >
          <!-- mb-margin bellow ma-margin above mx-margin from both side -->
          <hamburger/>
          </v-col>
          </v-row>
          <v-row class="hidden-md-and-up">
          <!-- <v-col sm="8"></v-col> -->
          <v-col sm="1" class="mb-sm-2 ma-sm-2 mb-2 ma-2 mx-0" >
          <!-- mb-margin bellow ma-margin above mx-margin from both side -->
          <searcicon/>
          </v-col>
          </v-row>
    </v-app-bar>

    <!-- Body -->
    <v-content light>
     
      <nuxt /> 
      <!-- a container is added in order to align it properly in all type of devices -->
      <v-container>
            <v-row justify="center">
        <v-col cols="10" sm="4" md="3">
           <Cards1/>
           </v-col>
           <v-col cols="10" sm="4" md="3">
             <Cards2/> 
           </v-col>
           <v-col cols="10" sm="4" md="3">
             <Cards3/> 
           </v-col>
          
      </v-row>
      <v-row justify="center" class="mx-sm-12 mx-12 ">
       <Button/> 
       </v-row>
      </v-container>
               </v-content>
    <!-- Footer -->
   

  </v-app>
</template>

