<template>
  <container>
    <v-col md="12" sm="12">
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
          src="icons-01.jpg">
        </v-img>

           <!-- src is the link of the image in the static -->
           <!-- max width and max height constrains the image within those dimentions -->
           <!-- md and sm helps in specifying the amount of space it will take in different screens eg. 
           sm is for i pad, md is for laptop screens, xs is for phones, etc -->
          <v-card-text class="text--primary">
          </v-card-text>

          <v-card-actions >
            <v-dialog v-model="dialog" persistent max-width="420" >
              <template v-slot:activator="{ on, attrs }">
                <v-btn md="6" sm="6"
                  block="true"
                  max-width="400"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on">
                  Apply for online debit card
                </v-btn> 
                <!-- text = true makes the button take the color of the background and makes the background invisible  -->
                <!-- block makes the button take maximum space available -->
                <!-- color blue darken two makes the blue a shade darker than the original -->
              </template>
              <v-card color="white darken-2" class="hey">
                <v-card-title 
                  
                  class="hey">
                  <h4> If you already have an active debit card, Please do not apply for debit card online </h4>
                </v-card-title>
                <!-- v-modal dialog is the mode/dialog pop up with width 420-->
                <!-- v-bind and v-on helps in opening the dialg hen the button is clicked -->
              <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn href="forms"
                    class="hey"
                    color="blue" 
                    text @click="dialog = false">ok
                  </v-btn>
                  <!-- href directs to a certain page -->
                  <!-- class hey is a custom defined class in the css which defines the color and font family to be used-->
                  <v-btn 
                    max-width="380"
                    color="blue" 
                    text @click="dialog = false">cancel
                  </v-btn>
                  <!-- href directs from one page to another when clicked on it -->
                </v-card-actions>
              </v-card>
           </v-dialog>

          </v-card-actions>
      </v-card>
   </v-col>
 </container>
</template>

<style> 
 .white--text {
    border: 1px solid;
  }

  .hey {
    color: rgb(47, 64, 143);
    font-family: Arial;
    }
  /* class hey helps in specifying the font and colour of the text used */

</style>