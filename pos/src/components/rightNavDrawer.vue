<template>
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
</template>
<script>
export default {
    name:'rightNavDrawer'
}
</script>
