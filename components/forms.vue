<template>
  <v-form v-model="isFormValid">
             <!--enabeling and disableing the submit button(validating) -->
    <v-container>
    
      <v-row>
         <h3 class="hey"> Online Debit Card Application </h3>
      </v-row>
         <v-divider color="red" width="240mm"> </v-divider>

             <!-- h3 and h4- sizes of the text -->
      <br>
             <!-- br is used to break the line and make the next component appear on the next line -->
      <v-layout row justify-center class="hey">
         <h4> <p class="text-center">CUSTOMER DETAILS </p> </h4>
          
      </v-layout>

      <v-row justify="center"> 
        <v-col cols="7" md="7" sm="7">
          <v-text-field ref="form"
            v-model="accountno"
            outlined
            rounded
            type="password"
            light fixed 
            :rules="accountRules"
            :counter="15"
            label="Account Number*"
            >
          </v-text-field> 
        </v-col>
      </v-row> 
             <!-- type password converts the content into bullets -->
             <!-- rules field according to the script enebles the reqired and the no. of characters required-->
             <!-- counter shows number of characters allowed to enter -->
             <!-- color black lighr fixed app creates a black outline around the component and makes it distinct  -->
             <!-- href is used to re direct to a different webpage -->
      <v-row justify="center"> 
        <v-col cols="7" md="7" sm="7">
          <v-text-field ref="form"
           v-model="reaccountno"
           light fixed app
            type="password"
            :rules="reaccountRules"
            :counter="15"
            label="Re-enter account Number*"
            outlined
            rounded>
          </v-text-field> 
        </v-col>
     </v-row> 

     <v-row justify="center">
        <v-col cols="7" md="7" sm="7"> 
          <v-text-field ref="form"
            v-model="email"
            light fixed app
            :rules="emailRules"
            label="Captcha*"
            outlined
            rounded >
          </v-text-field>
        </v-col>
     </v-row>
      <!-- sm md helps in defining the grids in a perticular screen type like sm is for ipads xs is for all the phones md i the laptop screen,etc -->
     <v-row justify="center">
        <v-col cols="3" md="4" sm="4">
          <v-img
           class="mx-auto"
           max-height="100px"
           max-width="220px"
           src="captcha.png">
          </v-img>
        </v-col>
      </v-row> 

      <v-row justify="center" >
         <em text id="require">*Required</em>
      </v-row>
            <!-- Justify center aligns it to the centre -->
            <!-- em text makes the text italic -->

      <v-card-actions >
        <v-dialog 
        v-model="dialog" 
        persistent height="300"
        width="300" 
        :rounded="rounded"
            >
           <template v-slot:activator="{ on, attrs }">
             <v-row justify="center">
               <v-col cols="1">  
                 <v-btn 
                   :disabled="!isFormValid"
                   color="#DA2627"
                   dark
                   rounded
                   v-bind="attrs"
                   v-on="on">
                    OK 
                 </v-btn> 
               </v-col>
             </v-row>
           </template>
            <!-- href directs form one page to another -->
            <!-- :disabled ensures that the button is disabled till the form is filled -->
            <!-- rounded makes the shape of the edges rounded -->
          <v-card color="white darken-2" class="hey">
            <v-btn href="forms" 
               
              icon dark @click="dialog = false">
                <v-icon>
                  mdi-close
                </v-icon>
            </v-btn>
            <!-- mdi is used before the icon name to enable it -->

              <v-card-title class="hey">
                <h3> Successfully Applied For Online Debit Card </h3>
              </v-card-title>
              <!-- class hey is the style made below to match the requirements -->
        
              <v-card-actions>
                <v-spacer></v-spacer>
                <!-- v-spacer adds space between two components in the row -->

                <v-btn href="mediacard"
                  color="blue" 
                  text @click="dialog = false">
                  ok
                </v-btn>
              </v-card-actions>
          </v-card>
       </v-dialog>
      </v-card-actions>

    </v-container>
  </v-form>
</template>

<style> 
  .hey {
    color: rgb(47, 64, 143);
    font-family: Arial;
  }
  /* .hey is used to make a class and #is used to create a unique set */

  .black--text {
    border: 1px solid;
  }

   #inspire {
    background-color: rgb(255, 255, 255);
    color: rgb(255, 255, 255);
  }
  
  #require {
    color: red;
    font-family: Arial;
  }

</style>

<script>

  export default {
    data: () => ({
      isFormValid: false,
      accountno: '',
      reaccountno: '',
      lastname: '',
      accountRules: [
        v => !!v || 'account number is required',
        v => v.length <= 15 || 'Name must be less than 15 characters',
      ],
      // ensures that the textfield is filled under the above conditions
      reaccountRules: [
        v => !!v || 're entering the account number is required',
        v => v.length <= 15 || 'Name must be less than 15 characters',
      ],

      email: '',
      emailRules: [
        v => !!v || 'Captcha is required',
      ],
    }),
  }
</script>