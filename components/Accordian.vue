<template>
<v-container>
<v-row>
  
<col cols="10" md="10" lg="10">
  <v-expansion-panels class="#9E9E9E">
  <v-expansion-panel class="blue darken-4"
   v-for="(featurs,a) in 1"
   
    :key="i"
  >
  <!--Accordian-->
  <!--feature,a is like giving a variable for more then one element-->
  <!--v-for allows to write in loop-->
 
    <v-expansion-panel-header> Features </v-expansion-panel-header>
      
    <v-expansion-panel-content> 
    
    <!--expansion panel helps in expanding a tab to an accordian-->
      <v-row><h4> PURPOSE</h4></v-row>
       <v-row>1. Purchase of new/old residential unit (house/ flat/villa/apartment etc.)</v-row> <v-row> 2. Construction of residential unit on exiting non agriculture plot.</v-row> <v-row>3. Purchase of non-agricultural plot and construction of residential unit (composite project) thereon**</v-row><v-row> 4. Repairs/ improvements/ extension of the existing residential property. </v-row> <v-row>5. Take-over of housing loan availed from another bank / FI </v-row><v-row> 6. Completion of under construction residential unit.</v-row> <v-row>7. Purchase of solar power panel along with purchase / construction of house.</v-row><v-row></v-row><br>
      <v-row><h4> ELIGIBILITY</h4> </v-row> <v-row> 1. Indian citizens and NRIs. </v-row><v-row>2. Minimum entry age is 18 years and maximum exit age up to 75 years.</v-row> <v-row>3. Individuals may apply singly or jointly with other eligible individuals.</v-row> <br>
      <v-row><h4> QUANTUM OF LOAN</h4></v-row><v-row> 1. No limit on the quantum of loan.</v-row>
      <v-row>2. Loan eligibility depending on repayment capacity of the borrower and value of property.</v-row>
      <v-row>3. Maximum loan amount for repairs/renovation is Rs.30 lakh.</v-row><br>
      <v-row><h4> REPAYMENT</h4></v-row> <v-row>1. Repayment period of up to 30 years in case of purchase/ construction</v-row>
      <v-row>2. Repayment period of 15 years in case of repair & renovation </v-row><br>
      <!--h1 standing for heading. it can be manipulated by changing numbers after h upto 6-->
    <checkboxfeatures/>
    </active class>
    </v-expansion-panel-content>
    
  </v-expansion-panel> 
  <v-row class="mt-md-4">
    
  <v-expansion-panel class="blue darken-4" 
    v-for="(forms,b) in 1"
    :key="i"
  >
    <v-expansion-panel-header>Forms and Documents</v-expansion-panel-header>
    <v-expansion-panel-content>
      <!--Cnten features-->
      
      <v-row><h4> LIST OF DOCUMENTS</h4> </v-row> <v-row><h5>1. Proof of identity (any of the following)</h5> </v-row><v-row>a. Passport</v-row>
       <v-row> b. PAN Card</v-row>
      <v-row>c. Employee identity card</v-row>
      <v-row>d. Any other valid proof</v-row><br> 
      <v-row><h5>Proof of identity (any of the following)</h5></v-row> <v-row>a. Electricity bill</v-row>
      <v-row>b. Telephone bill</v-row>
      <v-row>c. Aadhar</v-row>
      <v-row>d. Any other valid proof</v-row><br>
      <v-row><h5>2. PAN Card (any of the following)</h5> </v-row>
      <v-row><h5>3. Last 12 months bank statement</h5> </v-row>
      <v-row><h5>4. Proof of income</h5> </v-row>
      <v-row><h5>5. Proof of income</h5></v-row> <v-row> <h5>6. For salaried class</h5> </v-row> <v-row>a. Last one year ITR</v-row>
      <v-row>b. Form-16/ letter from Employe</v-row>
      <v-row>c. Last 6 months salary slip</v-row>
     <v-row>
  
<v-col cols="10" md="10" lg="10">
     <checkbox/>
     </v-col>
     </v-row>
    </v-expansion-panel-content>
  </v-expansion-panel> 
  </v-row>


  <!--In this checkbox box code is after the first accordian code to show it as a part of he accordian -->
  
  <v-expansion-panel class="blue darken-4" 
    v-for="(forms,c) in 1"
    :key="i"
  >
    <v-expansion-panel-header>FAQs</v-expansion-panel-header>
    <v-expansion-panel-content>
     
    <v-row><h4>Q.1 What is the maximum loan amount?</h4> </v-row>
The maximum amount of loan sanctioned would be minimum of A or B<br>

   <v-row>A. 90% for up to Rs.30 lakh, 80% for above Rs.30 lakh to up to Rs.75 Lakh & 75% for above Rs.75 lakh of the total cost of the house (which excludes stamp duty, registration fee, transfer fee, cost of furnishing, etc. if any)</v-row>
   B. Loan amount as per our eligibility calculations based on repayment capacity of the borrowers
   Note: The maximum loan amount would be decided by the repayment capacity of the borrower, which is determined mainly with reference to the present income. However, it should be borne in mind that besides present income, several factors like age, qualifications, spouse's income, present outgoing towards rent, future potential for earning higher income, present level of assets and liabilities of the borrowers, etc. will have a bearing on the repayment capacity of the borrower. In case the net take home income after all deductions (such as proposed EMI, taxes, Insurance premium and other out go) is not sufficient, the eligible amount of loan would then be reduced. The income of co-applicant can be added to that of the applicant to improve the repayment capacity.
   <v-row><h4>Q.2 Who can be the co-applicants for the home loan?</h4></v-row><v-row> <h5>Permitted co-applicants for male applicant :</h5></v-row>

<v-row>Wife</v-row>
<v-row>Father</v-row>
<v-row>Mother</v-row>
<v-row>Son</v-row>
<v-row>Daughter in law</v-row>
<v-row>Unmarried-daughter</v-row>
    </v-expansion-panel-content>
  </v-expansion-panel>
  </v-expansion-panels>
 
  <v-row justify="center" class="mt-md-4 mt-sm-4">
  <!--br is used to break sentences in the content-->

  <!--button-->  
  <div class="text-center">
  <v-btn href="homeloan"
  
   color="primary" dark>Ok</v-btn>
    </div>
  <!--href is used to specify URL of the page-->
  </v-col>
  </v-row>
  </v-container>
  </template>}
  <style>
  .features{
    color:white !important; 
    
  }
  </style>
  