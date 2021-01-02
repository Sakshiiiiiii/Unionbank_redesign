<template>
  <!--Your App Starts Here -->
  <v-app id="inspire">
    
    <!--Header -->
    
      
       <!-- Component Example -->
      
      
       
         
    

    <!-- Body -->
    <v-content light>
    <navbreadcrumb/>
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
       <EndButton/>
       
       <!-- <popup/> -->
       </v-row>
      </v-container>
               </v-content>
    <!-- Footer -->
   

  </v-app>
</template>