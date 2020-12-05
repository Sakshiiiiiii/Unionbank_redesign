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
<<<<<<< HEAD
    <v-card-text>
            <p class="display-1 text--primary">
        Features Of UDSA
      </p>
            <div span class="black--text">
       Any Resident Individual can open and operate 
=======
    <v-card-text >
    
        <h2>  
         Features Of UDSA </h2>
        <br>
      
      
            <div span class="black--text">
              <p>
      Any Resident Individual can open and operate 
>>>>>>> 297b6b048089ea1634c97f4635e9ad0fa10c96b2

Union Digital Savings Account (UDSA) in his 
/her name.<br>

Joint Account or Joint mandate for Operation is 
not permitted.<br>

No minimum balance requirement as account can 
be opened with Zero balance.<br>

Cash Deposit Charges will be applicable for any 
cash deposit in the account.<br>

Receipts through Digital Channel – Free and 
Unlimited.<br>

Outward Remittances charges through Digital 
Channels like U-mobile, UPI, BHIM, Net Banking 
etc- No Charges via all Digital Platforms.<br>

Redeem Points for Every On-Line Transaction.
</p>
      </div>
    </v-card-text>
    </v-alert>
  </v-card>
  </v-hover>
</template>