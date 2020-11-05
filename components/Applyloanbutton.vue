<template>
  <v-row justify="center">
    <!-- justify center will get the whole content in center -->
    <!-- isformvalid is for if condition that is if the users click the button only then he can proceed -->
          <!-- Disable will not allow the working of  button until a particular details are filled -->

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
  data() {
    return {
      dialog: false,
    };
  },
};
</script>