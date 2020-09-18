<template>
  <!--Your App Starts Here -->
  <v-app id="inspire">
    
    <!--Header -->
    <v-app-bar color="#E22026" dark fixed app>
      <!-- <v-toolbar-title>Application</v-toolbar-title> -->
       <!-- Component Example -->
      <Ubilogo/> <tab/>
    </v-app-bar> 

    <!-- Body -->
    <v-content light>
      <nuxt /> 
    </v-content> 
    <breadcrumb/>
    
    <!-- Footer -->
    <v-footer color="#E22026" app>
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
    background-color: white;
    color: rgb(255, 255, 255);
  }
</style>
