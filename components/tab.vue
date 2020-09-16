<template>
  <v-card>
    <v-tabs
      light
      background-color="#E22026"
      
    >
      <v-tabs-slider color="white"></v-tabs-slider>

      <v-tab
        v-for="i in 6"
        :key="i"
        :href="'#tab-' + i"
      >
        Item {{ i }}
      </v-tab>
    </v-tabs>
  </v-card>
</template>