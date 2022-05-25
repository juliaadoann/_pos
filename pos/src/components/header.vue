<template>
    <v-app-bar
      absolute
      color="white"
      elevate-on-scroll
      scroll-target="#scrolling-techniques-7"
    >

    <v-bottom-sheet
    v-model="sheet"
    inset
    >
    <template v-slot:activator="{ on, attrs }">
      <v-app-bar-nav-icon v-bind="attrs" v-on="on"></v-app-bar-nav-icon>
    </template>
    <v-sheet
    class="text-center"
    height = "900px"
    >
      <div class="my-3">
          Officiis debitis
        </div>
      <v-btn
          class="mt-6"
          text
          color="black"
          @click="sheet = !sheet"
        >
          close
        </v-btn>
    </v-sheet>
  </v-bottom-sheet>

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
        <v-icon v-bind="attrs" v-on="on">mdi-heart-outline</v-icon>
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


    <v-sheet>
      <v-container class="fill-height" fluid>
      <v-row
        align ="center"
        justify ="center"
      >
        <v-btn icon>
        <v-icon @click.stop="drawer = !drawer">mdi-dots-vertical</v-icon>
        </v-btn>
      </v-row>
    </v-container>


    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
    <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>
      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
            <v-divider></v-divider>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    </v-sheet>
  </v-app-bar> 
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
.drawer {
  height: 500px
}
</style>