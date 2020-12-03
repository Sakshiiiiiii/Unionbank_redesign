<template> 
  <div> 
    <v-content>
      
      <v-container>
        <bedrad />
        <v-row>
          <h3 class="hey">  Online Debit Card Application </h3>
         <!-- h3 helps in defining the size of the font  -->
         <!-- hey is a custom class made to define the color and fornt family of the component -->
        </v-row>
        <v-divider color="red" width="240mm"> </v-divider>
        
        <v-row  
          class="hey">
          <v-col md="6" sm="6" >
            <applydebit/>
          </v-col>
       
         <!-- the rows and columns help in placing the item in a perticular position and also to define its size -->
        
          <v-col md="6" sm="6" >
            <trackdebit/>
          </v-col>
        </v-row>
       
      </v-container>
      

    </v-content>
  </div>
</template> 

<script>
</script>

<style> 
.hey {
    color: rgb(47, 64, 143);
    font-family: Arial;
  }
/* .component is the format used to creat a custom class */
</style>