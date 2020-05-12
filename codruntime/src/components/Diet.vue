<template>
<v-card>
  <v-carousel height="450">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="getImgLink(item.src)"
      reverse-transition="fade-transition"
      transition="fade-transition"
    >
      <div class="dietinfo">
        <!-- <v-layout row class="ma-4">
          <v-flex xs6 sm6 md6>
              <v-card class="mx-auto" max-width="600" style="cursor:pointer" href="/athome">
                <v-img class="white--text align-end" height="200px" src="../assets/gym10.jpg">
                <v-card-title style="font-size:26px;">At Home</v-card-title>
                </v-img>
              </v-card>
          </v-flex>
          <v-flex xs6 sm6 md6>
                <v-card-title class="white--text" style="font-size:26px;">Personal Trainer</v-card-title>
          </v-flex>
        </v-layout> -->
         <div class="diettextinfo" style="color:white;margin:180px 100px;">
           <h2 style="font-size:55px">{{item.text}}</h2>
           <h2 style="font-size:26px">{{item.subtext}}</h2>
           <v-btn depressed small class="white--text" color="#3A6B1D" :href="item.route">{{item.text}}</v-btn>
         </div>
      </div>
    </v-carousel-item>
  </v-carousel>
</v-card>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'diet1.jpg', text: 'Contact', subtext: 'Nearby', route: '/contactnearby'
          },
          {
            src: 'diet2.jpg', text: 'Eat', subtext: 'feel Good', route: '/food'
          },
          {
            src: 'diet3.jpg', text: 'Work', subtext: 'Employment', route: '/employment'
          },
          {
            src: 'hero1.jpg', text: 'Farmers', subtext: 'for you', route: '/farmer'
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
