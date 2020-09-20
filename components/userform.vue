<template>
  <form>
    <v-text-field
      v-model="name"
      :error-messages="nameErrors"
      :counter="10"
      label="Name"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>

    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Surname"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>

    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Mobile No."
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>

    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Phone No."
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>
    
    <v-text-field
      v-model="email"
      :error-messages="emailErrors"
      label="E-mail"
      required
      @input="$v.email.$touch()"
      @blur="$v.email.$touch()"
    ></v-text-field>
    <v-select
      v-model="select"
      :items="items"
      :error-messages="selectErrors"
      label="Location"
      required
      @change="$v.select.$touch()"
      @blur="$v.select.$touch()"
    ></v-select>
    
     <v-row>
     <v-col cols="3">

    <v-img
      class="mx-auto"
      height="30px"
      width="160px"
      src="Captcha.jpg"
      
    >
     
    </v-img>

  </v-col>
  </v-row>
    <v-text-field
      v-model="Surname"
      :error-messages="nameErrors"
      :counter="10"
      label="Captcha"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>
    <v-checkbox
      v-model="isFormValid"
      :error-messages="checkboxErrors"
      label="I / We authorize Union Bank of India and its representatives to call me or SMS me with reference to my loan enquiry / application. "
      required
      @change="$v.checkbox.$touch()"
      @blur="$v.checkbox.$touch()"
    ></v-checkbox>

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
      <v-card>
        <v-card-title class="headline">Task Successful!</v-card-title>
        <v-card-text>Your loan application is succefully done.<br> Thank you for banking with us.</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          
          <v-btn color="green darken-1" text @click="dialog = false">Ok</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row> 
    
    
  </form>
</template>

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
      items: [
        'Nagpur',
        'Aurangabad',
        'Nashik',
        'Thane',
        'Kalyan',
        'Aurangabad',
        'Mumbai',
        'Navi Mumbai',
        'Delhi',
        'Bhiwandi',
        'Satara',
        'Panvel',
        'Lonavala',
        
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
        !this.$v.name.maxLength && errors.push('Item must be at most 10 characters long')
        !this.$v.name.required && errors.push('Item is required.')
        return errors
      },
      emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('Must be valid')
        !this.$v.email.required && errors.push('Item is required')
        return errors
      },
    },

    methods: {
      submit () {
        this.$v.$touch()
      },
      clear () {
        this.$v.$reset()
        this.name = ''
        this.email = ''
        this.select = null
        this.checkbox = false
      },
    },
  }
</script>