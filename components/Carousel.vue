   <template>
   <v-card 
        
        class="mx-auto"
        
        >
        
  <v-carousel :show-arrows="false"
        max-width="950"
        max-height="100">
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
            src: 'smile.png',
            
          },
          {
            src: 'ladka.png',
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