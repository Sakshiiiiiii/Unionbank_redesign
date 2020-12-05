<template>
<!-- the color class and width of the card is defined  -->
<!-- hover function is added to make it more similar to redesign -->
<!-- open delay is added -->
 <v-hover
 v-slot="{ hover }"
        open-delay="200">
        <!--the hover function is defined and given its properties  -->

  <v-card
  
  :elevation="hover ? 16 : 2"
          :class="{ 'on-hover': hover }"
          class="mx-auto"
          max-width="1200"
          color="#FFFFFF">
          <v-alert outlined color="#195289">
    
    <!-- paragraph tag is used to diffrentiate between the header and te rest of the text --> 
    <!-- another component is table which is anoter component-->
    <v-card-text >
    
        <h2>  
        Features Of SBGENs </h2>
        <br>
      
      
            <div span class="black--text">
              <p>
       Any Resident Individual - Single Accounts, Two or 
more individuals in Joint Accounts, Illiterate Persons, 
Visually Impaired persons, Purdanasheen Ladies,
Minors, Associations, Clubs, Societies, etc. <br>

Minimum balance requirement with or without 
cheque book facility:<br> 
</p>
<br>
<Table/>
<br>

      </div>
    </v-card-text>
    </v-alert>
  </v-card>
  </v-hover>
</template>