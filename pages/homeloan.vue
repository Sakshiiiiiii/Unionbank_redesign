<template>
  <div>
    <v-content>
      <v-container>
        <v-row>
          <v-col cols="1" md="1" sm="1"> </v-col>
          <!-- cols md and sm are sizes which helped me in making te website responsive -->
          <v-col cols="10" md="7" sm="10">
            <homeloan />
          </v-col>
          <v-col cols="0" md="3" sm="3" class="hidden-cols-only">
            <!-- Hidden cols will hide the image in xs -->
            <v-row class = "hidden-sm-and-down">
            <v-img src="loan.JPG"> </v-img>
            </v-row>
          </v-col>
          <v-col md="1"> </v-col>
        </v-row>
      </v-container>
    </v-content>
  </div>
</template>


