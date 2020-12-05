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
        Features Of SBPEN
      </p>
            <div span class="black--text">
       Eligibility: All customers who are drawing pension 
=======
    <v-card-text >
    
        <h2>  
         Features Of SBPEN </h2>
        <br>
      
      
            <div span class="black--text">
              <p>
     Eligibility: All customers who are drawing pension 
>>>>>>> 297b6b048089ea1634c97f4635e9ad0fa10c96b2
through our Bank or intend to draw pension through 
our Banks are eligible to open specially designed 
pension account under scheme code SBPEN.<br>

Prompt Disbursal of pensions to the pensioners.<br>

DA increases are given promptly.<br>

Interest is calculated on daily product basis and 
will be credited on quarterly basis in the months 
of April, July, October and January every year.<br>

Rate of interest up to 25 lacs - 3.25% p.a. and 
<<<<<<< HEAD
more than 25 lacs 4% p.a.<br> <br> <br> <br>

=======
more than 25 lacs 4% p.a.<br><br> <br> <br>
</p>
>>>>>>> 297b6b048089ea1634c97f4635e9ad0fa10c96b2
      </div>
    </v-card-text>
    </v-alert>
  </v-card>
  </v-hover>
</template>