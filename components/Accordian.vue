<template>
   
  <v-container>
    <div>
      <v-alert outlined color="#34618E">
        <v-row justify="center">
        <v-col cols="10" md="10" sm="10" class="px-md-8 mx-sm-4 mx-4">
        <!-- cols stand for mobile phones, where 10 means 10 column width/ md- laptop/ lg- computer  -->
        <!-- this are added for making the website responsive -->


        <!-- 1EXPAN -->


        <v-expansion-panels class="#9E9E9E">
          <!-- "panels stands for all expansion in accordion"  -->
          <v-expansion-panel
            class="grey lighten-2"
            v-for="(forms, a) in 1"
            :key="a"
          >
            <!--Accordian-->
            <!--feature,a is like giving a variable for more then one element-->
            <!--v-for allows to write in loop-->
            <v-expansion-panel-header color ="#00579D" text="black">
             Features </v-expansion-panel-header>
             
            <v-expansion-panel-content>
              <!-- v-expansion panel header color set the color of the headng -->
              <br>
              <!--expansion panel helps in expanding a tab to an accordian-->
              <h5>
              <a 
                class="text-decoration-none"
                >PURPOSE</a></h5>
              <v-divider color="red" width="60mm"> </v-divider><br />
              <v-row span class="black--text">
                <v-col md="10" sm="10" cols="10">
                  <ol>
                    <!-- ol is used to put the text in the pointerr form -->
                    <!-- li stands for list. It helps in forming a list  -->
                    <li>
                      Purchase of new/old residential unit (house/
                      flat/villa/apartment etc.)
                    </li>
                    <li>
                      Construction of residential unit on exiting non
                      agriculture plot.
                    </li>
                    <li>
                      Repairs/ improvements/ extension of the existing
                      residential property.
                    </li>
                    <li>
                      Take-over of housing loan availed from another bank / FI
                    </li>
                    <li>Completion of under construction residential unit.</li>
                    <li>
                      Purchase of solar power panel along with purchase /
                      construction of house.
                    </li>
                  </ol>
                </v-col>
              </v-row>
              <br />
              <h5>
                <a 
                class="text-decoration-none"
                >ELIGIBILITY</a></h5>
              <v-divider color="red" width="70mm"> </v-divider><br />
              <!-- divider helps in deviding 2 section with a thin line -->
              <v-row span class="black--text">
                <ol>
                  <li>Indian citizens and NRIs</li>
                  <li>
                    Minimum entry age is 18 years and maximum exit age up to 75
                    years.
                  </li>
                  <li>
                    Individuals may apply singly or jointly with other eligible
                    individuals.
                  </li>
                </ol>
              </v-row>
              <br />
              <h5>
                <a 
                class="text-decoration-none"
                >QUANTUM OF LOAN</a></h5>
                <v-divider color="red" width="125mm"> </v-divider>
              <br />
              <v-row span class="black--text">
                <ol>
                  <li>No limit on the quantum of loan.</li>
                  <li>
                    Loan eligibility depending on repayment capacity of the
                    borrower and value of property
                  </li>
                  <li>
                    Maximum loan amount for repairs/renovation is Rs.30 lakh.
                  </li>
                </ol>
              </v-row>
              <br />
              <h5>
                <a 
                class="text-decoration-none"
                >MARGIN, I.E. YOUR SHARE</a></h5>
              <v-divider color="red" width="160mm"> </v-divider><br />
              <v-row span class="black--text">
                <ol>
                  <li>
                    10% of the total cost of the purchase/ construction for
                    loans up to Rs.30 Lakhs
                  </li>
                  <li>
                    20% of the total cost of the purchase/ construction for
                    loans above Rs.30 lakhs and up to Rs.75 Lakhs.
                  </li>
                  <li>
                    25% of the total cost of the purchase/ construction for
                    loans Above Rs.75 Lakhs
                  </li>
                  <li>20% of total cost of the repairs/renovation.</li>
                </ol>
              </v-row>
              <br />
              <h5><a 
                class="text-decoration-none"
                >MORATORIUM PERIOD</a></h5>
              <v-divider color="red" width="140mm"> </v-divider><br />
              <v-row span class="black--text">
                <ol>
                  <li>
                    Moratorium period of up to 36 months in case of purchase/
                    construction
                  </li>
                  <li>
                    Moratorium period of to 12 months in case of repair &
                    renovation.
                  </li>
                </ol>
              </v-row>
              <br />
              <h5><a 
                class="text-decoration-none"
                >REPAYMENT</a></h5>
              <v-divider color="red" width="80mm"> </v-divider><br />
              <v-row span class="black--text">
                <ol>
                  <li>
                    Repayment period of up to 30 years in case of purchase/
                    construction.
                  </li>
                  <li>
                    Repayment period of 15 years in case of repair & renovation
                  </li>
                </ol>
              </v-row>
              <br />
              <h5><a 
                class="text-decoration-none"
                >REPAYMENT METHODS</a></h5>
              <v-divider color="red" width="145mm"> </v-divider><br />
              <v-row span class="black--text">
                <ol>
                  <li>Equated Monthly Installments (EMI)</li>
                  <li>
                    For borrowers engaged in agriculture or allied activities,
                    Equated Quarterly Instalment (EQI) instead of EMI may be
                    permitted.
                  </li>
                  <li>
                    Step-Up Repayment Method: EMI is set at a value lower than
                    the normal EMI for initial months and for the remaining
                    tenure it is set at a level higher than the normal EMI.
                  </li>
                  <li>
                    Balloon Repayment Method: lower than normal EMI at the start
                    of the repayment tenure followed by lump sum amount expected
                    to be available at end of repayment tenure.
                  </li>
                  <li>
                    Flexible Loan installment Plan (FLIP) Method: After receipt
                    some lumpsum amount midway the EMI for the remaining period
                    can be at a lower value than normal EMI.
                  </li>
                  <li>
                    ullet payment: Deposit of lump sum payment during the
                    repayment tenure and downward revision in EMIs for the
                    remaining tenure
                  </li>
                </ol>
              </v-row>
              <br />
              <h5><a 
                class="text-decoration-none"
                >SMART SAVE OPTION</a></h5>
              <v-divider color="red" width="140mm"> </v-divider><br />
              <v-row span class="black--text">
                <ol>
                  <li>
                    Under the Smart Save product, over and above the regular EMI
                    for the loan, customers can deposit additional amount with
                    an option to withdraw such excess amount at a later date as
                    per their requirement.
                  </li>
                  <li>
                    As the excess funds help in reducing the loan outstanding, a
                    lower interest is charged in the loan account (till such
                    excess funds are available in the account). In other words,
                    this option helps the customers to maximize their savings on
                    interest without sacrificing ones financial liquidity
                  </li>
                </ol>
              </v-row>
              <br />
              <h5><a 
                class="text-decoration-none"
                >GUARANTEE</a></h5>
               <v-divider color="red" width="80mm"> </v-divider><br />
              <v-row span class="black--text">
                <ol>
                  <li>
                    Third party guarantee is not required for Resident Indian.
                  </li>
                  <li>
                    One/two guarantors of Indian Residents, having means
                    equivalent to that of the loan amount, is to be provided by
                    the NRI applicant.
                  </li>
                </ol>
              </v-row>
              <br />
              <h5><a 
                class="text-decoration-none"
                >INSURANCE</a></h5>
             <v-divider color="red" width="75mm"> </v-divider><br />
              <v-row span class="black--text">
                <ol>
                  <li>
                    Property should be comprehensively insured for an amount not
                    less than the value of the property (less cost of land),
                    covering all risks with Bank clause.
                  </li>
                </ol>
              </v-row>
              <br />

              <!--h1 standing for heading. it can be manipulated by changing numbers after h upto 6-->
              <checkboxfeatures />
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
        <br /><br />


        <!-- 2EXPAN -->


        <v-expansion-panels>
          <v-expansion-panel
            class="grey lighten-2"
            v-for="(forms, b) in 1"
            :key="b"
          >
            <v-expansion-panel-header color ="#00579D" text="black" >Forms and Documents</v-expansion-panel-header
            >
            <v-expansion-panel-content>
              <br>
              <!--Content features-->

             <h5> <a
                class="text-decoration-none">
                LIST OF DOCUMENTS  </a></h5>
              <v-divider color="red" width="125mm"> </v-divider><br /><br />
             <v-row span class="black--text">
                
                <ol>
                  <h5>Proof of identity (any of the following)</h5>
                  <li>Passport</li>
                  <li>Pan Card</li>
                  <li>Employee identity card</li>
                  <li>Any other valid proof</li>
                  <br />
                  <h5>Proof of address (any of the following)</h5>
                  <li>Electricity bill</li>
                  <li>Telephone bill</li>
                  <li>Aadhar card</li>
                  <li>Any other valid proof</li>
                  <br />
                  <h5>PAN Card</h5>
                  <h5>Last 12 months bank statement</h5>
                  <h5>Additional document required for NRI</h5>
                  <h5>Copy of Visa stamped on the passport</h5>
                  <h5>Latest work permit</h5>
                  <h5>
                    Employment contract (if the contract is in any language
                    other than English, the same has
                  </h5>
                  <h5>
                    to be translated into English and attested by
                    Employer/Indian Embassy)
                  </h5>
                  <h5>
                    Any other document required as per the application form
                  </h5>
                </ol>
              </v-row>
              <br />

              <v-col cols="10" md="10" sm="10">
                <checkbox />
              </v-col>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
        <br /><br />


        <!-- 3EXPAN -->


        <v-expansion-panels>
          <!--In this checkbox box code is after the first accordian code to show it as a part of he accordian -->

          <v-expansion-panel
            class="grey lighten-2"
            v-for="(forms, c) in 1"
            :key="c"
          >
            <v-expansion-panel-header color ="#00579D" text="black">FAQs</v-expansion-panel-header>
            <v-expansion-panel-content>
              <br>
             <h4><a 
                class="text-decoration-none"> Q.1 What is the maximum loan amount? </a></h4> 
              <v-divider color="red" width="300mm"> </v-divider>
              <v-row span class="black--text">
              The maximum amount of loan sanctioned would be minimum of A or
              B<br />

              
               A. 90% for up to Rs.30 lakh, 80% for above Rs.30 lakh to up to
                Rs.75 Lakh & 75% for above Rs.75 lakh of the total cost of the
                house (which excludes stamp duty, registration fee, transfer
                fee, cost of furnishing, etc. if any) <br><br>
                
              
              B. Loan amount as per our eligibility calculations based on
              repayment capacity of the borrowers Note: The maximum loan amount
              would be decided by the repayment capacity of the borrower, which
              is determined mainly with reference to the present income.
              However, it should be borne in mind that besides present income,
              several factors like age, qualifications, spouse's income, present
              outgoing towards rent, future potential for earning higher income,
              present level of assets and liabilities of the borrowers, etc.
              will have a bearing on the repayment capacity of the borrower. In
              case the net take home income after all deductions (such as
              proposed EMI, taxes, Insurance premium and other out go) is not
              sufficient, the eligible amount of loan would then be reduced. The
              income of co-applicant can be added to that of the applicant to
              improve the repayment capacity.

              <br /><br />
              </v-row>
              <h4><a 
                class="text-decoration-none">
                  Q.2 Who can be the co-applicants for the home loan? </a>
                </h4>
              <v-divider color="red" width="400mm"> </v-divider>
              <v-row span class="black--text">
              Permitted co-applicants for male applicant :
              </v-row>
              <v-row span class="black--text">
              <ol>
                <li>Wife</li>
                <li>Father</li>
                <li>Mother</li>
                <li>Son</li>
                <li>Daughter in law</li>
                <li>Unmarried-daughter</li>
              </ol>
              </v-row>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>

        <v-row justify="center" class="mt-md-4 mt-sm-4 mt-4">
          <!--br is used to break sentences in the content-->

          <!--button-->
          <div class="text-center">
            <v-btn rounded href="homeloan" color="primary" dark>Ok</v-btn>
          </div>
          <!--href is used to specify URL of the page-->
        </v-row>
        </v-col>
        </v-row>
      </v-alert>
    </div>
  </v-container>
</template>}

    <style>
.features {
  color: rgb(10, 10, 10) !important;
}
</style>