<template>
        <v-layout row mx-4 wrap center>
          <v-flex xs6 sm6 md6 v-for="(item,i) in items" :key="i" class="pa-2">
              <v-card class="mx-auto" max-width="600" style="cursor:pointer" :href="item.route">
                <v-img class="white--text align-end" height="200px" :src="getImgLink(item.src)">
                <v-card-title style="font-size:26px;">{{item.text}}</v-card-title>
                </v-img>
              </v-card>
          </v-flex>
        </v-layout>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'farmer1.jpg', text: 'Farmer', subtext: 'Healthy Recipes', route: '/farmer'
          },
          {
            src: 'farmer2.jpg', text: 'Employment', subtext: 'feel Good', route: '/employment'
          },
          {
            src: 'farmer3.jpg', text: 'Food', subtext: 'Sweat Achieve',  route: '/food'
          },
          {
            src: 'farmer4.jpg', text: 'Transportation', subtext: 'to be fit', route: '/transport'
          },
           {
            src: 'farmer5.jpg', text: 'Geo fencing', subtext: 'Sweat Achieve', route: '/geofencing'
          },
          {
            src: 'farmer6.jpg', text: 'Thermal Scanning', subtext: 'to be fit', route: '/thermal'
          },
        ],
      }
    },
    methods: {
        getImgLink(pic){
            return require('../assets/' + pic)
        }
    }
  }
</script>
