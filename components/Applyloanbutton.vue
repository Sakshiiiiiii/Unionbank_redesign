<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="290">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
        :disabled="!isFormValid"
    
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Apply Loan
        </v-btn>
      </template>
      
    </v-dialog>
  </v-row>
</template>

<script>
  export default {
    data () {
      return {
        dialog: false,
      }
    },
  }
</script>