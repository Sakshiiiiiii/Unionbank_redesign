<template>
  <div>
    <v-breadcrumbs :items="items">
      <template v-slot:divider>
        <v-icon color="grey">mdi-chevron-right</v-icon>
        <!--For changing code-->
      </template>
    </v-breadcrumbs>
  </div>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          text: 'Home',
          disabled: false,
          href: 'breadcrumbs_dashboard',
        },
        //false stands for directing 'home' to previous link
        {
          text: 'Products',
          disabled: false,
          href: 'breadcrumbs_link_1',
        },
        {
          text: 'Loans',
          disabled: false,
          href: 'breadcrumbs_link_2',
        },
        {
          text: 'Homeloan',
          disabled: true,
          href: 'breadcrumbs_link_3',
        },
      ],
    }),
  }
</script>
