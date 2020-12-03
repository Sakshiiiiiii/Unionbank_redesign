   <template>
   <v-card 
        color="white"
        class="mx-auto"
        width="170"
        height="150"
        >
<v-alert outlined color="#D32F2F"> 
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
</v-alert>
     </v-card>   
     </template> 