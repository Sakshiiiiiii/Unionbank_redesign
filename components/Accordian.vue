{    <template>
  <v-expansion-panels>
  <v-expansion-panel
    v-for="(featurs,a) in 1"
    :key="i"
  >
  <!--feature,a is like giving a variable for more then one element-->
  <!--v-for allows to write in loop-->
    <v-expansion-panel-header>Features</v-expansion-panel-header>
    <v-expansion-panel-content>
    <!--expansion panel helps in expanding a tab to an accordian-->
      <h4> PURPOSE</h4> <br> 1. Purchase of new/old residential unit (house/ flat/villa/apartment etc.)<br> 2. Construction of residential unit on exiting non agriculture plot.<br> 3. Purchase of non-agricultural plot and construction of residential unit (composite project) thereon**<br> 4. Repairs/ improvements/ extension of the existing residential property.<br> 4. Take-over of housing loan availed from another bank / FI <br> 5. Completion of under construction residential unit.<br> 6. Purchase of solar power panel along with purchase / construction of house.<br><br>
      <h4> ELIGIBILITY</h4> <br> 1. Indian citizens and NRIs. <br>2. Minimum entry age is 18 years and maximum exit age up to 75 years.<br> 3. Individuals may apply singly or jointly with other eligible individuals. <br> <br>
      <h4> QUANTUM OF LOAN</h4> <br> 1. No limit on the quantum of loan.<br>
      2. Loan eligibility depending on repayment capacity of the borrower and value of property.<br>
      3. Maximum loan amount for repairs/renovation is Rs.30 lakh.<br><br>
      <h4> REPAYMENT</h4> <br>1. Repayment period of up to 30 years in case of purchase/ construction<br>
      2. Repayment period of 15 years in case of repair & renovation<br>
      <!--h1 standing for heading. it can be manipulated by changing numbers after h upto 6-->
    <checkboxfeatures/>
    </v-expansion-panel-content>
  </v-expansion-panel> 
  <v-expansion-panel
    v-for="(forms,b) in 1"
    :key="i"
  >
    <v-expansion-panel-header>Forms and Documents</v-expansion-panel-header>
    <v-expansion-panel-content>
      <h4> LIST OF DOCUMENTS</h4> <br> <h5>1. Proof of identity (any of the following)</h5> <br>a. Passport<br>
      b. PAN Card<br>
      c. Employee identity card<br>
      d. Any other valid proof<br><br> 
      <h5>Proof of identity (any of the following)</h5> <br>a. Electricity bill<br>
      b. Telephone bill<br>
      c. Aadhar<br>
      d. Any other valid proof<br><br>
      <h5>2. PAN Card (any of the following)</h5> <br>
      <h5>3. Last 12 months bank statement</h5> <br>
      <h5>4. Proof of income</h5> <br>
      <h5>5. Proof of income</h5> <br> <h5>6. For salaried class</h5> <br> a. Last one year ITR<br>
      b. Form-16/ letter from Employer<br>
      c. Last 6 months salary slip<br>

     <checkbox/>
    </v-expansion-panel-content>
  </v-expansion-panel> <br>
  <!--In this checkbox box code is after the first accordian code to show it as a part of he accordian -->
  
  <v-expansion-panel
    v-for="(forms,c) in 1"
    :key="i"
  >
    <v-expansion-panel-header>FAQs</v-expansion-panel-header>
    <v-expansion-panel-content>
    <h4>Q.1 What is the maximum loan amount?</h4> <br>
The maximum amount of loan sanctioned would be minimum of A or B<br>

   A. 90% for up to Rs.30 lakh, 80% for above Rs.30 lakh to up to Rs.75 Lakh & 75% for above Rs.75 lakh of the total cost of the house (which excludes stamp duty, registration fee, transfer fee, cost of furnishing, etc. if any)<br>
   B. Loan amount as per our eligibility calculations based on repayment capacity of the borrowers
   Note: The maximum loan amount would be decided by the repayment capacity of the borrower, which is determined mainly with reference to the present income. However, it should be borne in mind that besides present income, several factors like age, qualifications, spouse's income, present outgoing towards rent, future potential for earning higher income, present level of assets and liabilities of the borrowers, etc. will have a bearing on the repayment capacity of the borrower. In case the net take home income after all deductions (such as proposed EMI, taxes, Insurance premium and other out go) is not sufficient, the eligible amount of loan would then be reduced. The income of co-applicant can be added to that of the applicant to improve the repayment capacity.<br><br>
   <h4>Q.2 Who can be the co-applicants for the home loan?</h4><br> <h5>Permitted co-applicants for male applicant :</h5><br>

Wife<br>
Father<br>
Mother<br>
Son<br>
Daughter in law<br>
Unmarried-daughter<br>

    </v-expansion-panel-content>
  </v-expansion-panel>
  <!--br is used to break sentences in the content-->

    
  <br><div class="text-center">
  <v-btn href="homeloan"
  rounded color="primary" dark>Ok</v-btn>
    </div>
  <!--href is used to specify URL of the page-->
  </v-expansion-panels>
  </template>}