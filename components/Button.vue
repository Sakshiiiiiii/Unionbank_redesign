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
    <v-btn md="6" sm="6"
                  block="true"
                  max-width="400"
                  text="true"
                  color="blue darken-2"
                  dark
                  v-bind="attrs"
                  v-on="on">
                  Apply
                </v-btn> 
                </template>
              <v-card color="white darken-2" class="hey">
                <v-card-title class= "hey">
                  <h3> I have read all the features and understood them.  </h3>
                </v-card-title>
                <!-- v-modal dialog is the mode/dialog pop up with width 420-->
                <!-- v-bind and v-on helps in opening the dialg hen the button is clicked -->
              <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn href="index"
                    class="hey"
                    color="blue" 
                    text @click="dialog = false">Yes
                  </v-btn>
                  <!-- href directs to a certain page -->
                  <!-- class hey is a custom defined class in the css which defines the color and font family to be used-->
                  <v-btn href="accountsavin"
                    max-width="380"
                    color="blue" 
                    text @click="dialog = false">No
                  </v-btn>
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
    
  <!-- </form> -->
</template>

<script>
  import { validationMixin } from 'vuelidate'
  import { required, maxLength, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
         
      checkbox: {
        checked (val) {
          return val
        },
      },
    },

    data: () => ({
      
      checkbox: false,
    }),

    computed: {
      checkboxErrors () {
        const errors = []
        if (!this.$v.checkbox.$dirty) return errors
        !this.$v.checkbox.checked && errors.push('Must Check to proceed ')
        return errors
      },
      },

    methods: {
      submit () {
        this.$v.$touch()
      },
      clear () {
        this.$v.$reset()
        this.checkbox = false
      },
    },
  }
</script>