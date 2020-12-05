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
          <v-col sm="1" class="mb-sm-2 ma-sm-2 mb-8 ma-2 mx-0" >
          <!-- mb-margin bellow ma-margin above mx-margin from both side -->
          <hamburger/>
          </v-col>
          </v-row>
        <!-- <v-col class="hidden-sm-and-down"> -->
          <!-- </v-col> -->
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
      
        <nuxt /> 
      </v-content> 
      
      
      <!-- Footer -->
      <v-footer
     class= "mt-lag-16 mt-md-16 mt-sm-16 mt-16"
     color="#DA2627"
  >
  <v-container>
    <v-row>
      <v-col
       cols="12"
       sm= "2"
       md= "3"
       >

       <h3> About Us </h3>
       <v-divider> </v-divider>
       <br>
       <font size= "2"> 
         Overview <br> 
         Other Stakeholders' <br>
         Information <br>
         Investor Relations <br>
         News Room <br>
         Corporate Governance <br>
         Careers <br>
         CSR <br>
         Regulatory Disclosures <br>
       </font>
      </v-col>
      
       <v-col
       cols="12"
       sm= "2"
       md= "2"
       > 

       <h3> Useful Links </h3>
       <v-divider> </v-divider>
       <br>
       <font size= "2"> 
         Privacy <br> 
         Important messages <br>
         Apply for Credit Card <br>
         Quick Links <br>
         Citizen's Charter <br>
         Login to NetBanking <br>
         Terms and Conditions <br>
         Website Usage Terms <br>
         Sitemap <br>
         Security <br>
         US Patriot Act Certificate <br>
         Our Corporate commitment <br>
       </font>
      </v-col>

      <v-col
       cols="12"
       sm= "2"
       md= "2"
       >

       <h3> Resources </h3>
       <v-divider> </v-divider>
       <br>
       <font size= "2"> 
         We care for you <br> 
         Glossary <br>
         Watch Videos <br>
         Learning Centre <br>
         Important Notices <br>
         Form centre <br>
         Fees and Charges <br>
         Rates <br>
         Online Services <br>
       </font>
      </v-col>

      <v-col
       cols="12"
       sm= "2"
       md= "3"
       >

       <h3> Need Help </h3>
       <v-divider> </v-divider>
       <br>
       <font size= "2"> 
         FAOs <br> 
         Customer Care <br>
         Contact Us <br>
         Use of Unparlimentary <br>
         Language By Customers <br>
         Active Channel Partners <br>
         DNC Dedupe <br>
         Locate Us <br>
         Do-Not-Call-Registration <br>
       </font>
      </v-col>

      <v-col
       cols="12"
       sm= "2"
       md= "2"
       >

       <h3> Connect with us on </h3>
       <v-divider> </v-divider>
       <br>
      <v-container>
        <v-row>

          <v-col cols="12" sm="3" md="3">
          <v-btn icon >
            <v-icon> mdi-instagram </v-icon>
          </v-btn> 

          <v-btn icon >
            <v-icon> mdi-whatsapp </v-icon>
          </v-btn>
          
          </v-col>

          <v-col cols="12" sm="3" md="3">
            <v-btn icon >
            <v-icon> mdi-facebook </v-icon>
          </v-btn>

          <v-btn icon >
            <v-icon> mdi-youtube </v-icon>
          </v-btn>

          </v-col>

          <v-col cols="12" sm="3" md="3">
            <v-btn icon >
            <v-icon> mdi-twitter </v-icon>
          </v-btn>

          <v-btn icon size="42px">
            <v-icon> mdi-linkedin </v-icon>
          </v-btn>

          </v-col>
        </v-row>

        <v-row>
          <v-btn text="true"> Report a Fraud </v-btn>
        </v-row>
      </v-container> 
      </v-col>
   </v-row>

  </v-container>
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
      background-color: #ffffff;
      color: rgb(46, 65, 143);
    }
  </style>
