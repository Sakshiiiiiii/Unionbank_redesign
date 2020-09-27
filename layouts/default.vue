<template>
  <!--Your App Starts Here -->
  <v-app id="inspire">
    
    <!--Header -->
    <v-app-bar color="#E22026" dark fixed app>
      <!-- <v-toolbar-title>Application</v-toolbar-title> -->
       <!-- Component Example -->
      <Ubilogo/> 
       <v-row class="hidden-sm-and-down">

      <tab/> 
      </v-row>
      <v-row class="hidden-sm-and-down">
      <v-img
      class="mx-auto"
      src= "textbox.jpg">
      </v-img>
      </v-row>
      <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
       </v-btn>
      
    </v-app-bar> 

    <!-- Body -->
    <v-content light>
    <navbreadcrumb/>
      <nuxt /> 
    </v-content> 
    
    
    <!-- Footer -->
    <v-footer color="#E22026" app>
    <v-img
    class="mx-auto"
    src="footernav.jpg">
    </v-img>
      <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
      </v-footer>

  </v-app>
</template>

<script>
export default {}
</script>

<style> 
  .white--text {
    border: 1px solid;
  }

   #inspire {
    background-color: #9E9E9E;
    color: rgb(255, 255, 255);
  }
</style>
