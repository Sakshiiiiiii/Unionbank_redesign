<template>
  <div class="text-center" flat>
    <!-- open on click command allows the card to show options when clicked -->
    <v-menu
      open-on-hover
      color="white" light           
      top
      offset-y>
      <!-- the slot is activated when clicked -->
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="#FF0000"
          dark
          v-bind="attrs"
          v-on="on"
          height="48"
          width="20">
          <!-- a hamburger icon is added to make it easier for the user to understand -->
          <!-- icon is used from static -->
           <img
    class="Asset5"
    alt="Asset5"
    src="Asset5.png"
  >
          
        </v-btn>
      </template>

      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>
// the items are defined 
<script>
  export default {
    data: () => ({
      items: [
        { title: 'PRODUCTS' },
        { title: 'DIGITAL BANKING' },
        { title: 'INTERNATIONAL RELATIONS' },
        { title: 'WE CARE' },
        { title: 'CONTACT US' },
        { title: 'ABOUT US' },
      ],
    }),
  }
</script>
// dimensions of the icon is defined
<style>
.Asset1 {
  height: 30px;
  width: 30px;
}
</style>
