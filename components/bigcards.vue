  <template>
  <v-row>
    <!-- changed the colour  -->
    <v-col md="12" sm="12" offset-sm="center">
      <v-card class="mx-auto" max-width="520" color="#223C77" rounded="rounded">
        <v-img src="Health-Insurance-renew.png" height="360px"></v-img>

        <v-card-title class="font-weight-regular" style="font-family:Segoe UI"> Lifeline Health Insurance </v-card-title>

        <v-card-subtitle>
          Protection plans that works best for you and your family.
        </v-card-subtitle>

        <!-- the lines are broken with <br> -->
        <v-card-text class="text justify ;font-weight-regular" style="font-family:Segoe UI" >
          Lifeline is a holistic plan from Royal Sundaram that covers the health
          insurance needs of you and your family.<br /><br />
          * 100% Reload of Sum Insured at no extra cost.<br /><br />
          * Double your Sum Insured in 5 claim free years.
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    show: true,
  }),
};
</script>