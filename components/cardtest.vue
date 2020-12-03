   <template>
   <v-container>
      <v-row >
        <v-col
          v-for="card in cards"
          :key="card.text"
          :cols="card.flex"
        >
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
          {{card.src}}>

          <v-card-title v-text="card.title"></v-card-title>
        </v-img>
<v-btn md="6" sm="6"
                  block="true"
                  max-width="160"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on">
                  {{card.text}}
                </v-btn>
  </v-alert>           
     </v-card>
        </v-col>
      </v-row>
    </v-container>
      
     
</template> 

<script>
  export default {
    data: () => ({
      cards: [
        {  src: 'Applyonline.png', flex: 3 , text: 'apply online'},
        {  src: 'DebitCard.png', flex: 3, text: 'debit card'},
        {  src: 'Location.png', flex: 3, text: 'location' },
        {  src: 'Onlinepayment.png', flex: 3, text: 'online payment' },
        {  src: 'Rates.png', flex: 3, text: 'rates' },
        {  src: 'Onlinebanking.png', flex: 3, text: 'online banking' },
      ],
    }),
  }
</script>

  

