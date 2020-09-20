<template>
  <v-treeview
    selectable
    selected-color="blue"
    :items="items"
  ></v-treeview>
</template>

<script>
  export default {
    data: () => ({
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