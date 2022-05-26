<template>
  <v-menu
  open-on-hover
  offset-y
  bottom right
  >
    <template v-slot:activator="{ on, attrs }">
        <v-card-text style="height: 100px; width: 80px; position: relative">
            <v-fab-transition>
              <v-btn
                v-show="!hidden"
                color="grey enlighten-1"
                class="button"
                fixed left bottom
                dark
                absolute
                fab
                v-bind="attrs"
                v-on="on"
              >
                <v-icon>mdi-forum</v-icon>
              </v-btn>
            </v-fab-transition>
          </v-card-text>
        </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
  </v-menu>
</template>
<script>
export default {
    name:'fabButton',
    data: () => ({
      items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
      ]
    })
}
</script>
<style scoped>
.button {
  margin-bottom: 40px
}
</style>