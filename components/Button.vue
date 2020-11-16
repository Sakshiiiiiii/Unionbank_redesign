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
    >
    <!-- class color and click is defined -->
    </v-checkbox>
       <v-btn
    color="#195289"
      class="mr-4"
      @click="submit"
    >
      submit
    </v-btn>
    
  </form>
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