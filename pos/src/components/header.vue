<template>
<div>
    <v-app-bar
      absolute
      color="white"
      elevate-on-scroll
      scroll-target="#scrolling-techniques-7"
    >
    <v-btn icon>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    </v-btn>

      <v-icon>home</v-icon>
      <v-toolbar-title >Home</v-toolbar-title>

      <v-spacer></v-spacer>

      <div style="margin-top: 30px; margin-right: 20px">
        <v-autocomplete
        v-model="values"
              :items="locations"
              outlined
              dense
              label="Lorem ipsum">
        </v-autocomplete>
      </div>

    <v-dialog
      v-model="dialog"
      width="500px">
      <template v-slot:activator="{ on, attrs }">
        <v-btn icon
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>mdi-note-text-outline</v-icon>
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5" style="font-weight: bold">Order History</span>
        </v-card-title>
        <v-divider></v-divider>
        <v-container>
        <v-row>
        <v-col
        cols="12"
        sm="6"
        md="9">
        <v-text-field 
        label="Tel"
        outlined
        dense
        prepend-inner-icon="mdi-phone"></v-text-field>
        </v-col>
        <v-col
        cols="12"
        sm="6"
        md="2">
        <v-btn type="submit">SUBMIT</v-btn>
        </v-col>
        </v-row>
        </v-container>
        <v-card-text style="height: 300px">
          Lorem ipsum dolor sit amet
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="black"
            text
            @click="dialog = false"
          >
            Close
          </v-btn>
        </v-card-actions>
      </v-card>
      </v-dialog>

      <v-dialog
      v-model="dialog"
      width="500px">
      <template v-slot:activator="{ on, attrs }">
        <v-btn icon
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>mdi-heart-outline</v-icon>
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5" style="font-weight: bold">Loves</span>
        </v-card-title>
        <v-divider></v-divider>
        <v-card-text style="padding-top: 20px">
          Lorem ipsum dolor sit amet
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="black"
            text
            @click="dialog = false"
          >
            Continue Shopping
          </v-btn>
        </v-card-actions>
      </v-card>
      </v-dialog>

    <v-dialog
      v-model="dialog"
      width="500px">
      <template v-slot:activator="{ on, attrs }">
        <v-btn icon
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>mdi-cart-outline</v-icon>
        </v-btn>
      </template>
      <v-card>
        <v-container style="height: 70px">
        <v-row>
        <v-col
        cols="12"
        sm="12"
        md="9">
        <v-card-title>
          <span class="text-h5" style="font-weight: bold">Cart</span>
        </v-card-title>
        </v-col>
        <v-col>
          <v-card-subtitle>
          <span>View all</span>
        </v-card-subtitle>
        </v-col>
        </v-row>
        </v-container>
        <v-divider></v-divider>
        <v-card-text style="padding-top: 20px">
          Lorem ipsum dolor sit amet
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="black"
            text
            @click="dialog = false"
          >
            Continue Shopping
          </v-btn>
          <v-btn
            color="black"
            text
            @click="dialog = false"
          >
            View Cart & Checkout
          </v-btn>
        </v-card-actions>
      </v-card>
      </v-dialog>


    <v-bottom-sheet
    v-model="sheet"
    inset
    >

    <template v-slot:activator="{ on, attrs }">
      <v-btn icon>
        <v-icon v-bind="attrs" v-on="on">mdi-flag-outline</v-icon>
      </v-btn>
    </template>
    <v-sheet
    class="text-center"
    height = "200px"
    >
    <v-btn
          class="mt-6"
          text
          color="black"
          @click="sheet = !sheet"
        >
          close
        </v-btn>
        <div class="my-3">
          Officiis debitis
        </div>
    </v-sheet>
  </v-bottom-sheet>

  <v-btn icon @click.stop="drawer = !drawer">
        <v-icon >mdi-dots-vertical</v-icon>
  </v-btn>
  
    
  </v-app-bar>
  <v-navigation-drawer
      v-model="drawer"
      absolute
      bottom
      temporary
      right
      height="100vh"
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="black--text text--accent-4"
        > 
        <v-list-item-title>Lorem ipsum</v-list-item-title>
        <v-divider></v-divider>
        <div v-for="item in dropdownitems" :key="item">
          <v-list-item>
            <v-list-item-title>{{item}}</v-list-item-title>
          </v-list-item>
        </div>
        </v-list-item-group>
      </v-list>
  </v-navigation-drawer>

  </div>
 
</template>


<script>
export default {
    name:  'myHeader',
    data () {
      return {
        drawer: null,
        locations: [
        'Sapien',
        'El punto',
        'Textos',
        'Contrario',
        'Contenido',
        'Sólo',
        'Esencialmente',
        'Phasellus',
        'Sapien',
        'El punto',
        ]
      }
    }
    
}
</script>
<style scoped>

</style>