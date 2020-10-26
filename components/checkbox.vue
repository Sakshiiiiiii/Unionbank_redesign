<template>
<v-form v-model="isFormValid" >
  <!-- isformvalid is for if condition that is if the users click the button only then he can proceed -->
  <!-- selected color in 6 line will change the color of the box of the checkbox when selected -->
  <v-treeview
    selectable
    selected-color="red"
    
    :items="items"
  ></v-treeview>
  </v-form>
</template>

<script>
  export default {
    data: () => ({
      isFormValid: false,
      items: [
        {
          id: 1,
          name: 'Yes, I know the forms and documents required.',
          // name contains the content of the checkbox 
          children: [
            { id: 2, name: 'Calendar : app' },
            { id: 3, name: 'Chrome : app' },
            { id: 4, name: 'Webstorm : app' },
          ],
        },
         ],
    }),
  }
</script>