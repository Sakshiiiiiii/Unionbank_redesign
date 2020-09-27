<template>
<v-form v-model="isFormValid">
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
          name: 'Yes, I have read the features of Home Loan.',
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