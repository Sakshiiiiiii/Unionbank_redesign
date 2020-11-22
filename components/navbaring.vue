<template>
  <v-tabs
  
    
  <v-tabs color="white"
  background-color="#E22026"
    dark
  >
    <v-tab>
      PRODUCTS
    </v-tab>
    <v-tab>
      DIGITAL BANKING
    </v-tab>
    <v-tab>
      INVESTOR RELATION
    </v-tab>
    <v-tab>
     ABOUT US
    </v-tab>
    <v-tab>
      OTHERS
    </v-tab>
    <v-tab>
      WE CARE
    </v-tab>
    <!-- v-tab is ised to make the tabs -->

    <v-col
          cols="12"
          sm="2"
          md="3"
        >
          <v-text-field
            label="search"
            color="black" light fixed app
            solo
          ></v-text-field>

        <!-- label is the text that would appear on the text field beffow the user fills the field -->
        <!-- color black light fixed app creates a black outline around the component to make it more distinct  -->
        <!-- cols sm md helps in making the searchfield responsive -->
        </v-col>  
    <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
  </v-tabs>
</template>
