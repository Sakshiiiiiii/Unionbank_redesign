<template>

<v-container>
<v-row>
<v-col>
  <form>
    
 
    <v-alert
      outlined
      color="#34618E"
     >
    <!-- div alert is used to give n outlined retangle which contains a form -->
            <!-- item=a in line 18 is like giving a variable to the label -->
       
      <v-select
      
        v-model="select" 
        :items="a" 
        :error-messages="selectErrors"
        color="red" light fixed app
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
      color="red" light fixed app
      label="Interest rate (%)"
      
      required
      @change="$v.select.$touch()"
      @blur="$v.select.$touch()"
    ></v-select>
     <v-select
     
      v-model="isFormValid"
      
      :items="c"
      :error-messages="selectErrors"
      color="black" light fixed app
      label="Tenure (Years)"
      required
      @change="$v.select.$touch()"
      @blur="$v.select.$touch()"
    ></v-select>
    <!-- isformvalid (line38) is for if condition that is if the users click the button only then he can proceed -->

    <!-- </v-card>  -->
    </v-alert>
    
    <div class="text-left"> 
    <radio/> <br>
    </div>
  
  <!-- rounded is for round shaped buttons -->
  <div class="text-center"> 
    <v-btn
        rounded href="userform"
        
        :disabled="!isFormValid"
    
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        > 
        OK
        </v-btn>

    
    <v-btn rounded href="accordian"
    @click="clear">Back</v-btn>
  </div>  
   
  </form>
  
  </v-col>
  </v-row>
  </v-container>
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
      isFormValid:false,
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
