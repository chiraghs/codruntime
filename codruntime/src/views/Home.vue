<template>
  <div id="home" class="grey darken-4">
    <v-parallax
    height="600"
    src="../assets/diet4.jpg"
    >
      <div class="herotext" style="margin-left:100px;">
        <h1 class="hero1" style="font-size:30px">We are in this together</h1>
        <h1 class="hero2" style="font-size:50px">Stay Home <span class="subh2" style="color:#3A6B1D">Stay Safe</span></h1>
        <h1 class="hero3" style="font-size:50px"><span style="color:#3A6B1D">Stay Skilled</span></h1>
        <!-- <v-layout row mx-1>
          <v-flex xs3 sm3 md1 mx-2>
            <v-btn depressed small class="white--text" color="#3A6B1D" href="/consult">Consult</v-btn>
          </v-flex>
          <v-flex xs4 md1 style="margin-left:20px">
            <v-btn depressed small class="white--text" color="#3A6B1D" href="/store">Store</v-btn>
          </v-flex>
        </v-layout> -->
      </div>
  </v-parallax>

  <!-- <div class="section2">
        <v-layout row class="ma-4 pa-1">
          <v-flex xs6 sm6 md6>
              <v-card class="mx-auto" max-width="600" style="cursor:pointer" href="/athome">
                <v-img class="white--text align-end" height="200px" src="../assets/gym10.jpg">
                <v-card-title style="font-size:26px;">At Home</v-card-title>
                </v-img>
              </v-card>
          </v-flex>
          <v-flex xs6 sm6 md6  >
            <v-card class="mx-auto" max-width="600"  style="cursor:pointer" href="/personaltrainer">
                <v-img class="white--text align-end" height="200px" src="../assets/gym3.jpg">
                <v-card-title style="font-size:26px;">Personal Trainer</v-card-title>
                </v-img>
            </v-card>
          </v-flex>
        </v-layout>
  </div> -->

  <div class="section3" style="margin-top:50px;">
    <Gymforms/>
  </div>

  <div class="section3" style="margin-top:50px;">
    <Diet/>
  </div>




  </div>
</template>

<script>
  export default {
    data () {
      return {

      }
    },
    components: {
      Diet: () => import('@/components/Diet'),
      Gymforms: () => import('@/components/gymform'),
    }
  }
</script>

<style scoped>

@media only screen and (max-width: 650px) {
   .hero-text{
     text-align: center;
  }
  .herotext .hero1{
    font-size: 20px;
  }
  .herotext .hero2 h1{
    font-size: 25px;
  }
  .herotext .hero2 .subh2{
    font-size: 35px;
    color: white;
  }
  .herotext .hero3 span{
    font-size: 35px;
  }
}
</style>