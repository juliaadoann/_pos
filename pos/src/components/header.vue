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
              :items="dropdownitems"
              outlined
              dense
              label="Lorem ipsum">
        </v-autocomplete>
      </div>

    <v-bottom-sheet
    v-model="sheet"
    inset
    >
    <template v-slot:activator="{ on, attrs }">
      <v-btn icon>
        <v-icon v-bind="attrs" v-on="on">mdi-note-outline</v-icon>
      </v-btn>
    </template>
    <v-sheet
    class="text-center"
    height = "400px"
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

    <v-bottom-sheet
    v-model="sheet"
    inset
    >
    <template v-slot:activator="{ on, attrs }">
      <v-btn icon>
        <v-icon v-bind="attrs" v-on="on">mdi-heart-outline</v-icon>
      </v-btn>
    </template>
    <v-sheet
    class="text-center"
    height = "400px"
    >
      <div>
          Officiis debitis
        </div>
    </v-sheet>
    </v-bottom-sheet>

    <v-bottom-sheet
    v-model="sheet"
    inset
    >
    <template v-slot:activator="{ on, attrs }">
      <v-btn icon>
        <v-icon v-bind="attrs" v-on="on">mdi-cart-outline</v-icon>
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

  <v-btn icon>
        <v-icon @click.stop="drawer = !drawer">mdi-dots-vertical</v-icon>
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
        items: [
          { title: 'Home', icon: 'mdi-view-dashboard' },
          { title: 'About', icon: 'mdi-forum' },
        ],
        dropdownitems: [
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