<template>
    <v-stepper v-model="e6" vertical dark>
      <v-stepper-step color="#3A6B1D" :complete="e6 > 1" step="1">
        Day 1, Monday
      </v-stepper-step>
  
      <v-stepper-content step="1" color="#3A6B1D">
        <v-card color="grey darken-1" class="mb-12" height="200px">
            <p style="margin:20px"><b>BREAKFAST</b>: Orange Juice - 3/4 Cup, Oatmeal - 1/2 Cup. </p>
            <p style="margin:20px"><b>LUNCH</b>: Vegetable Soup - 150 ml, Wheat Bread - 2, Apple - 1</p>
            <p style="margin:20px"><b>AFTERNOON SNACK</b>: Muffin - 1 </p>
            <p style="margin:20px"><b>DINNER</b>: Chicken Breast - 1/2/ Baked Potato - 1, Brown Rice.</p>
            <p style="margin:20px"><b>DESSERT</b>: Banana - 1</p>
        </v-card>
        <v-btn color="#3A6B1D" @click="e6 = 2">Continue</v-btn>
        <v-btn text>Cancel</v-btn>
      </v-stepper-content>
  
      <v-stepper-step color="#3A6B1D" :complete="e6 > 2" step="2">Day 2, Tuesday</v-stepper-step>
  
      <v-stepper-content color="#3A6B1D" step="2">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
            <p style="margin:20px"><b>BREAKFAST</b>: Orange Juice - 3/4 Cup, Oatmeal - 1/2 Cup. </p>
            <p style="margin:20px"><b>LUNCH</b>: Vegetable Soup - 150 ml, Tuna Sandwiches - 2, Apple - 1</p>
            <p style="margin:20px"><b>AFTERNOON SNACK</b>: Muffin - 1 </p>
            <p style="margin:20px"><b>DINNER</b>: Chicken Breast - 1/2/ Baked Potato - 1, Brown Rice.</p>
            <p style="margin:20px"><b>DESSERT</b>: Skim Milk - 150ml</p>
        </v-card>
        <v-btn color="#3A6B1D" @click="e6 = 3">Continue</v-btn>
        <v-btn text>Cancel</v-btn>
      </v-stepper-content>
  
      <v-stepper-step color="#3A6B1D" :complete="e6 > 3" step="3">Day 3, Wednesday</v-stepper-step>
  
      <v-stepper-content color="#3A6B1D" step="3">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
            <p style="margin:20px"><b>BREAKFAST</b>: Orange Juice - 3/4 Cup, Oatmeal - 1/2 Cup. </p>
            <p style="margin:20px"><b>LUNCH</b>: Vegetable Soup - 150 ml, Tuna Sandwiches - 2, Apple - 1</p>
            <p style="margin:20px"><b>AFTERNOON SNACK</b>: Muffin - 1 </p>
            <p style="margin:20px"><b>DINNER</b>: Chicken Breast - 1/2/ Baked Potato - 1, Brown Rice.</p>
            <p style="margin:20px"><b>DESSERT</b>: Banana - 1</p>
        </v-card>
        <v-btn color="#3A6B1D" @click="e6 = 4">Continue</v-btn>
        <v-btn text>Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-step color="#3A6B1D" :complete="e6 > 4" step="4">Day 4, Thursday</v-stepper-step>

      <v-stepper-content color="#3A6B1D" step="4">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
            <p style="margin:20px"><b>BREAKFAST</b>: Orange Juice - 3/4 Cup, Oatmeal - 1/2 Cup. </p>
            <p style="margin:20px"><b>LUNCH</b>: Vegetable Soup - 150 ml, Tuna Sandwiches - 2, Apple - 1</p>
            <p style="margin:20px"><b>AFTERNOON SNACK</b>: Muffin - 1 </p>
            <p style="margin:20px"><b>DINNER</b>: Chicken Breast - 1/2/ Baked Potato - 1, Brown Rice.</p>
            <p style="margin:20px"><b>DESSERT</b>: Banana - 1</p>
        </v-card>
        <v-btn color="#3A6B1D" @click="e6 = 5">Continue</v-btn>
        <v-btn text>Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-step color="#3A6B1D" :complete="e6 > 5" step="5">Day 5, Friday</v-stepper-step>

      <v-stepper-content color="#3A6B1D" step="5">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
            <p style="margin:20px"><b>BREAKFAST</b>: Orange Juice - 3/4 Cup, Oatmeal - 1/2 Cup. </p>
            <p style="margin:20px"><b>LUNCH</b>: Vegetable Soup - 150 ml, Tuna Sandwiches - 2, Apple - 1</p>
            <p style="margin:20px"><b>AFTERNOON SNACK</b>: Muffin - 1 </p>
            <p style="margin:20px"><b>DINNER</b>: Chicken Breast - 1/2/ Baked Potato - 1, Brown Rice.</p>
            <p style="margin:20px"><b>DESSERT</b>: Banana - 1</p>
        </v-card>
        <v-btn color="#3A6B1D" @click="e6 = 6">Continue</v-btn>
        <v-btn text>Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-step color="#3A6B1D" :complete="e6 > 6" step="4">Day 6, Saturday</v-stepper-step>

      <v-stepper-content color="#3A6B1D" step="6">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
            <p style="margin:20px"><b>BREAKFAST</b>: Orange Juice - 3/4 Cup, Oatmeal - 1/2 Cup. </p>
            <p style="margin:20px"><b>LUNCH</b>: Vegetable Soup - 150 ml, Tuna Sandwiches - 2, Apple - 1</p>
            <p style="margin:20px"><b>AFTERNOON SNACK</b>: Muffin - 1 </p>
            <p style="margin:20px"><b>DINNER</b>: Chicken Breast - 1/2/ Baked Potato - 1, Brown Rice.</p>
            <p style="margin:20px"><b>DESSERT</b>: Banana - 1</p>
        </v-card>
        <v-btn color="#3A6B1D" @click="e6 = 6">Continue</v-btn>
        <v-btn text>Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-step color="#3A6B1D" step="7">Day 7, Sunday</v-stepper-step>
      <v-stepper-content color="#3A6B1D" step="7">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
            <p style="margin:20px"><b>BREAKFAST</b>: Orange Juice - 3/4 Cup, Oatmeal - 1/2 Cup. </p>
            <p style="margin:20px"><b>LUNCH</b>: Vegetable Soup - 150 ml, Tuna Sandwiches - 2, Apple - 1</p>
            <p style="margin:20px"><b>AFTERNOON SNACK</b>: Muffin - 1 </p>
            <p style="margin:20px"><b>DINNER</b>: Chicken Breast - 1/2/ Baked Potato - 1, Brown Rice.</p>
            <p style="margin:20px"><b>DESSERT</b>: Skim Milk - 150 ml</p>
        </v-card>
        <v-btn color="#3A6B1D">Finished</v-btn>
      </v-stepper-content>
    </v-stepper>
  </template>

  <script>
    export default {
      data () {
        return {
          e6: 1,
        }
      },
    }
  </script>