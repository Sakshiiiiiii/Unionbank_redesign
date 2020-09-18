<template>
  <div>
    <v-breadcrumbs :items="items"></v-breadcrumbs>

   
  </div>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          text: 'Home',
          disabled: true,
          href: 'breadcrumbs_dashboard',
        },
        {
          text: 'Products',
          disabled: true,
          href: 'breadcrumbs_link_1',
        },
        {
          text: 'Loan',
          disabled: true,
          href: 'breadcrumbs_link_2',
        },
      ],
    }),
  }
</script>
