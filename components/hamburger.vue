<template>
      <!-- open on hover is like i changes a bit will there is a curser on it -->

  <div class="text-center">
    <v-menu
      open-on-hover
      top
      offset-y
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="#E12228"
          dark
          v-bind="attrs"
          v-on="on"
          height="40"
          width="20"
        >
          menu
          <!-- menu is like a hamburger used in the website-->
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

<script>
  export default {
    data: () => ({
      // items is like a list of things
      items: [
        { title: 'PRODUCTS' },
        { title: 'DIGITAL BANKING' },
        { title: 'INVESTOR RELATION' },
        { title: 'ABOUT US' },
        { title: 'OTHERS' },
        { title: 'CONTACTS' },
      ],
    }),
  }
</script>
