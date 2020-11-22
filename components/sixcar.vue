   <template>
   <v-card 
        color="white"
        class="mx-auto"
        width="170"
        height="115"
        >
 <v-img
          md="6" sm="6"
          contain="false"
          class="mx-auto"
          max-height="80px"
          max-width="110"
          src="Location.png">
        </v-img>
<v-btn md="6" sm="6"
                  block="true"
                  max-width="160"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on">
                  Location
                </v-btn>
     </v-card>   
     </template> 