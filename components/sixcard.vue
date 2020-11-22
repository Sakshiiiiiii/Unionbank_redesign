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
          src="DebitCard.png">
        </v-img>
<v-btn 
        href="debitcard" md="6" sm="6"
                  block="true"
                  max-width="160"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on">
                  Debit Card
                </v-btn>
     </v-card>   
     </template> 