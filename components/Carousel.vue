   <template>
   <v-card 
        
        class="mx-auto"
        
        >
        
  <v-carousel :show-arrows="false"
        
       height="300">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
   </v-card>
</template>
<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'ladka.png',
            
          },
          {
            src: 'smile.png',
          },
          {
            src: 'thumbsup.png',
          },
          {
            src: 'family.jpg',
          },
        ],
      }
    },
  }
</script>