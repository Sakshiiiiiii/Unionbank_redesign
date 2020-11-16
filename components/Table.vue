<template>
  <v-simple-table light >
   <!-- the elements of the table are grouped row wise -->
    <template v-slot:default>
      <!-- each tr tag repersents one row -->
      <thead>
        <tr>
          <th class="text-left">Centers</th>
          <th class="text-left">Without Cheque Book</th>
          <th class="text-left">With Cheque Book</th>
        </tr>
        <tr>
          <th class="text-left">Metro</th>
          <th class="text-left">500</th>
          <th class="text-left">1000</th>
        </tr>
        <tr>
          <th class="text-left">Urban</th>
          <th class="text-left">500</th>
          <th class="text-left">1000</th>
        </tr>
        <tr>
          <th class="text-left">Semi Urban</th>
          <th class="text-left">250</th>
          <th class="text-left">500</th>
        </tr>
        <tr>
          <th class="text-left">Rural</th>
          <th class="text-left">250</th>
          <th class="text-left">500</th>
        </tr>
      </thead>
          
      <!-- table is listed in one of the cards to represent data visually -->
    </template>
  </v-simple-table>
</template>


