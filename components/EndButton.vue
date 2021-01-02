<template>
  <form> 
    <!--the validated checkbox is taken from form -->
    <!--label shows the text to be displayed   -->

      <v-checkbox 
        v-model="checkbox"
        color="black" light fixed app
        :error-messages="checkboxErrors"
        label="I have read all the above features and understood them ."
        required
        @change="$v.checkbox.$touch()"
        @blur="$v.checkbox.$touch()"
        @click="isFormValid=true"
      >
      <!-- class color and click is defined -->
      </v-checkbox>
      <v-dialog
        v-model="dialog"
      >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          rounded
          :disabled="!isFormValid"
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Apply 
        </v-btn>
      </template>
                  
        <v-card class="white">
          <div class="text-center">
            <strong class="blue--text text--darken-4">
              <v-card-title class="headline"
                ><h5>Task Successful!</h5></v-card-title
              >
            </strong>
          </div>
          <strong class="blue--text text--darken-4">
            <v-card-text
              >Your loan application is successfully done.<br />
              Thank you for banking with us.</v-card-text
            >
          </strong>
          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn
              color="blue darken-1"
              text
              @click="dialog = false"
              rounded
              >Ok
              </v-btn
            >
          </v-card-actions>
        </v-card> 
    </v-dialog>
    
  </form>
</template>

<script>
  import { validationMixin } from "vuelidate";
  import { required, maxLength, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
         
      checkbox: {
        checked (val) {
          return val;
        },
      },
    },

    data: () => ({
      
      checkbox: false,
      dialog: false,
    }),

    computed: {
     checkboxErrors() {
      const errors = [];
      if (!this.$v.checkbox.$dirty) return errors;
      !this.$v.checkbox.checked && errors.push("You must agree to continue!");
      // The above text in orange is a sort of alert which users get when they fail to fill a particular section in a form
      return errors;
      },
      },

     methods: {
    submit() {
      this.$v.$touch();
    },
      
      clear() {
      this.$v.$reset();
      
      this.select = null;
      this.checkbox = false;
      },
    },
  }
</script>
