<<<<<<< HEAD
=======
<template>
  <!-- <form> -->
    <!--the validated checkbox is taken from form -->
    <!--label shows the text to be displayed   -->

      <!-- <v-checkbox 
      v-model="checkbox"
      color="black" light fixed app
      :error-messages="checkboxErrors"
      label="I have read all the above features and understood them ."
      required
      @change="$v.checkbox.$touch()"
      @blur="$v.checkbox.$touch()"
    > -->
    <!-- class color and click is defined -->
    <!-- </v-checkbox>
       <v-btn
    color="#195289"
      class="mr-4"
      @click="submit"
    > -->

    
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
                  
                  <strong class="blue--text text--darken-4">
                    <v-card-text
                      >Make sure you have read and understood all features before proceeding.</v-card-text
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
                    <v-btn
                      color="blue darken-1"
                      text
                      @click="dialog = false"
                      rounded
                      >Cancel
                      </v-btn
                    >
                  <!-- href directs from one page to another when clicked on it -->
                </v-card-actions>
              </v-card>
           </v-dialog>

          </v-card-actions>
      </v-card>
   </v-col>
 </container>

      <!-- submit
    </v-btn> -->
    
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
>>>>>>> 297b6b048089ea1634c97f4635e9ad0fa10c96b2
