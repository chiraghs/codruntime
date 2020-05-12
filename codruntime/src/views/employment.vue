<template>
  <div id="home" class="grey darken-4">
  <div class="section2">
        <v-layout row mx-4 center>
          <v-flex xs12 sm12 md6 v-for="(item,i) in items" :key="i" class="pa-1">
              <v-card
    class="mx-auto"
    color="grey darken-3"
    dark
    max-width="800"
  >

    <v-card-text class="headline font-weight-bold">
        {{item.Name}}
    </v-card-text>
    <v-card-text class="headline font-weight-bold">
        {{item.Date}}
    </v-card-text>
    <v-card-text class="headline font-weight-bold">
        {{item.infojob}}
    </v-card-text>
    <v-icon class="ml-4">mdi-map</v-icon>
    <span xs-small class="subheading">{{item.City}}</span>

    <v-card-actions>
      <v-list-item class="grow">
        <v-list-item-avatar color="grey darken-3">
          <v-img
            class="elevation-6"
            src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
          ></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title></v-list-item-title>
        </v-list-item-content>

        <v-row
          align="center"
          justify="end"
        >
          <v-icon class="mr-1">mdi-phone</v-icon>
          <span class="subheading mr-2">{{item.Phone}}</span>
        </v-row>
      </v-list-item>
    </v-card-actions>
  </v-card>
          </v-flex>
        </v-layout>

  </div>

  <div class="section3">
    <Diet class="ma-6"/>
  </div>

  </div>
</template>

<script>
import db from '@/fb'
  export default {
    data () {
      return {
          items: [ ],
      }
    },
    components: {
      Diet: () => import('@/components/Diet'),
    },
    created() {
      db.collection('events').onSnapshot(res => {
        const changes = res.docChanges();

        changes.forEach(change => {
          if(change.type === 'added'){
            this.items.push({
              ...change.doc.data(),
              id: change.doc.id
            })
          }
        })
      })
    }
  }
</script>
