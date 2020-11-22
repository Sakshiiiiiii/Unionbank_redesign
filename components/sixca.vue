   <template>
   <v-card 
        color="white"
        class="mx-auto"
        max-width="500"
        >
 <v-img
          md="6" sm="6"
          contain="false"
          class="mx-auto"
          max-height="300px"
          max-width="400"
          src="Onlinepayment.png">
        </v-img>
<v-btn md="6" sm="6"
                  block="true"
                  max-width="400"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on">
                  Online Payment
                </v-btn>
     </v-card>   
     </template> 