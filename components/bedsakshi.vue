<template>
  <div>
    <v-breadcrumbs
      text id="require"
      :items="items"
      large
      color="black" light fixed app 
    ></v-breadcrumbs>

    <!-- color black light fixed adds a black outline to the component -->
    <!-- items is the customised style made to match the style of the rest of the components -->
  </div>
</template>
<script>
import homeloanVue from '../pages/homeloan.vue'
import AccordianVue from './Accordian.vue'
  export default {
    data: () => ({
      items: [
        {
          text: 'Home',
          disabled: false,
         
        },
        {
          text: 'Homeloans',
          disabled: false,
          href: Accordian
        },
        {
          text: 'Amount Required',
          disabled: false,
          href: homeloan
        },
        {
          text: 'Form',
          disabled: false,
          href: 'Accordian'
        },
        
        
      ],
    }),
  }
</script>

<style scoped>
#require {
    color: red;
    font-family: Arial;
  }
  /* require helps in defining the font and colour of the component */

</style>