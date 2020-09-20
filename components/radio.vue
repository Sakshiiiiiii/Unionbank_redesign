<template>
  <v-card id="create">
    <v-container fluid>
      <v-row justify="center">
       
        <!-- <v-col cols="3" sm="6" md="3"> -->
          <!-- <v-subheader >Select the Sum Insured</v-subheader> -->
           <v-radio-group row v-model="transition" hide-details>
            <v-col>
            <v-radio value="slide-y-transition" label="New User"></v-radio>
            </v-col>
             <v-col>
            <v-radio value="slide-y-reverse-transition" label="Existing User"></v-radio>
            </v-col>
            
           </v-radio-group>
        <!-- </v-col> -->
      </v-row>
    </v-container>
     <v-speed-dial
      v-model="fab"
      :top="top"
      :bottom="bottom"
      :right="right"
      :left="left"
      :direction="direction"
      :open-on-hover="hover"
      :transition="transition"
    ></v-speed-dial> 
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      direction: 'top',
      fab: false,
      fling: false,
      hover: false,
      tabs: null,
      top: false,
      right: true,
      bottom: true,
      left: false,
      transition: 'slide-y-reverse-transition',
    }),

    computed: {
      activeFab () {
        switch (this.tabs) {
          case 'one': return { class: 'purple', icon: 'account_circle' }
          case 'two': return { class: 'red', icon: 'edit' }
          case 'three': return { class: 'green', icon: 'keyboard_arrow_up' }
          default: return {}
        }
      },
    },

    watch: {
      top (val) {
        this.bottom = !val
      },
      right (val) {
        this.left = !val
      },
      bottom (val) {
        this.top = !val
      },
      left (val) {
        this.right = !val
      },
    },
  }
</script>

<style>
  /* This is for documentation purposes and will not be needed in your application */
  #create .v-speed-dial {
    position: absolute;
  }

  #create .v-btn--floating {
    position: relative;
  }
</style>

