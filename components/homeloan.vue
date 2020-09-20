<template>
<v-row>
<v-col md="11">
  <form>
    
   
    
    <v-select
      v-model="select"
      :items="a"
      :error-messages="selectErrors"
      label="Loan Amount (Rs.)"
      required
      @change="$v.select.$touch()"
      @blur="$v.select.$touch()"
    ></v-select>
    <!--item can be any thing and it can be given a varible if there are more then one element-->
    
     <v-select
      v-model="select"
      :items="b"
      :error-messages="selectErrors"
      label="Interest rate (%)"
      required
      @change="$v.select.$touch()"
      @blur="$v.select.$touch()"
    ></v-select>
     <v-select
      v-model="isFormValid"
      :items="c"
      :error-messages="selectErrors"
      label="Tenure (Years)"
      required
      @change="$v.select.$touch()"
      @blur="$v.select.$touch()"
    ></v-select>
    <radio/> <br>
    
    
    
    <v-btn href="userform"
    
     class="mr-4" @click="submit">Ok</v-btn>
    
    <v-btn href="accordian"
    @click="clear">Back</v-btn>
  </form>
  </v-col>
  </v-row>
</template>
<!--href accordian is to link home page button to accordian-->
<script>
  import { validationMixin } from 'vuelidate'
  import { required, maxLength, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
      name: { required, maxLength: maxLength(10) },
      email: { required, email },
      select: { required },
      checkbox: {
        checked (val) {
          return val
        },
      },
    },

    data: () => ({
      name: '',
      email: '',
      select: null,
      a: [
        '5,00,000/-',
        '10,00,000/-',
        '50,00,000/-',
        '1,00,00,000/-',
          
      ],

      b: [
        '8%',
        '10%',
        '12%',
        '15%',
      ],
      c: [
        '5',
        '10',
        '15',
        '20',
      ],
      checkbox: false,
    }),
    
    
    
    computed: {
      checkboxErrors () {
        const errors = []
        if (!this.$v.checkbox.$dirty) return errors
        !this.$v.checkbox.checked && errors.push('You must agree to continue!')
        return errors
      },
      
      selectErrors () {
        const errors = []
        if (!this.$v.select.$dirty) return errors
        !this.$v.select.required && errors.push('Item is required')
        return errors
      },
      nameErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.maxLength && errors.push('Name must be at most 10 characters long')
        !this.$v.name.required && errors.push('Name is required.')
        return errors
      },
      emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('Must be valid e-mail')
        !this.$v.email.required && errors.push('E-mail is required')
        return errors
      },
  // The above text in orange appears when the user fails to fill the text field 
    },

    methods: {
      Ok () {
        this.$v.$touch()
      },
      Back () {
        this.$v.$reset()
        this.name = ''
        this.email = ''
        this.select = null
        this.checkbox = false
      },
    },
  }
</script>