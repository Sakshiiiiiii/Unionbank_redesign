<template>
  <v-expansion-panels>
    <v-expansion-panel
      v-for="(Features,a) in 1"
      :key="a"
    >
      <v-expansion-panel-header>Features</v-expansion-panel-header>
      <v-expansion-panel-content>
        
      </v-expansion-panel-content>
    </v-expansion-panel>
    <v-expansion-panel
      v-for="(Forms,b) in 1"
      :key="b"
    >
      <v-expansion-panel-header>Forms and Documents</v-expansion-panel-header>
      <v-expansion-panel-content>
        <feature accordian/>
      </v-expansion-panel-content>
    </v-expansion-panel>
     <v-expansion-panel
      v-for="(Forms,b) in 1"
      :key="b"
    >
      <v-expansion-panel-header>FAQs</v-expansion-panel-header>
      <v-expansion-panel-content>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </v-expansion-panel-content>
    </v-expansion-panel>
    
  </v-expansion-panels>
</template>