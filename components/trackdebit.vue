<template>
  <container>
    <v-col md="12" sm="12">
      <v-card 
        color="white"
        class="mx-auto"
        width="500"
        >
          <v-img
            contain="false"
            class="mx-auto"
            max-height="300px"
            max-width="400"
            src="icons-02.jpg">
          </v-img>
          <!-- src is the link of the image in the static -->
           <!-- max width and max height constrains the image within those dimentions -->
          <v-card-text 

            class="text--primary">
            
          </v-card-text>

          <v-card-actions>
            <v-dialog v-model="dialog" persistent max-width="420">
              <template v-slot:activator="{ on, attrs }">
                <v-btn 
                  
                  :disabled= true
                  max-width="380"
                  block="true"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on" >
                  Online Debit Card Tracking
                </v-btn> 
              </template>
            </v-dialog>
          </v-card-actions>
      </v-card>
   </v-col>
 </container>
</template>

<style scoped>
  
  #require {
    color: blue;
    font-family: Arial;
  }

</style>