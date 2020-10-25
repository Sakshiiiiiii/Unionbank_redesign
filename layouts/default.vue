  <template>
    <!--Your App Starts Here -->
    <v-app id="inspire">
      
      <!--Header -->
      <v-app-bar color="#E22026" dark fixed app>
        <!-- <v-toolbar-title>Application</v-toolbar-title> -->
        <!-- Component Example -->
        
        <Ubilogo/> 
        <v-col>
          </v-col>
        <v-row class="hidden-sm-and-down">
          <!-- tab will be hidden in sm(i pad) and other big screen. It is only for mobile screen -->
          <tab/> 
        </v-row>
        <v-row class="hidden-md-and-up">
          <v-col sm="8"></v-col>
          <v-col sm="1" class="mb-sm-2 ma-sm-2 mb-2 ma-2 mx-0" >
          <!-- mb-margin bellow ma-margin above mx-margin from both side -->
          <hamburger/>
          </v-col>
          </v-row>
        <v-col class="hidden-sm-and-down">
          </v-col>
          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
        </v-btn>
      <v-row  justify="end" class="  col-md-2 col-xs-1 col-sm-2">
       <v-text-field
        rounded
            v-model="search"
            clearable
            flat
            solo-inverted
            hide-details
            class="hidden-xs-only"
            label="Search"
           
          ></v-text-field>
          </v-row>

        
        
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
      background-color: #c4c4c4;
      color: rgb(46, 65, 143);
    }
  </style>
