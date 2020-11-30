   <template>
   <v-card 
        color="white"
        class="mx-auto"
        width="170"
        height="150"
        >
 <v-alert outlined color="#D32F2F">
 <v-img
          
          contain="false"
          class="mx-auto"
          max-height="80px"
          max-width="110"
          src="Onlinebanking.png">
        </v-img>
        
<v-btn 
                  block="true"
                  max-width="160"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on">
                  Online Banking
                </v-btn>
 </v-alert>
     </v-card>   
     </template> 