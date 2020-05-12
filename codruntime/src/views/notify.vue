<template>
<div>
<v-card dark>
        <v-card-title>
          <span class="headline">NOtify Custom Directive</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12" sm="6" md="4">
                <v-text-field label="First name*" required></v-text-field>
              </v-col>
              <v-col cols="12" sm="6" md="4">
                <v-text-field label="Last name" ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6" md="4">
                <v-text-field
                  label="Phone Number*" hint="we use your Phone number to contact you"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Email" hint="we use your Email to contact you"></v-text-field>
              </v-col>
              <v-col cols="12" sm="4" md="4">
                <v-text-field label="Home City" required></v-text-field>
              </v-col>
              <v-col cols="12" sm="4" md="4">
                <v-text-field label="Current City" ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-select dark class="dark"
                  :items="['0-17', '18-29', '30-54', '54+']"
                  label="Number of People gathered*"
                  required
                ></v-select>
              </v-col>
            </v-row>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer><!--
          <v-btn color="blue darken-1" text @click="dialog = false">Close</v-btn><v-dialog -->
      <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on }">
        <v-btn
          color="red lighten-2"
          dark
          v-on="on"
        >
          Submit
        </v-btn>
      </template>

      <v-card>
        <v-card-title
          class="headline grey lighten-2"
          primary-title
        >Thank you
        </v-card-title>

        <v-card-text>
          sent to respective directive they will look through
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="dialog = false"
          >
            Ok
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-card-actions>
      </v-card>

    </div>
</template>

<script>
  export default {
    data () {
      return {
          dialog: false,
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
