<template>
        <v-card-text style="height: 100px; position: relative">
            <v-fab-transition>
              <v-btn
                v-show="!hidden"
                color="grey enlighten-1"
                class="button"
                fixed left bottom
                dark
                absolute
                fab
              >
                <v-icon>mdi-cart-outline</v-icon>
              </v-btn>
            </v-fab-transition>
          </v-card-text>
</template>
<script>
export default {
    name:'fabButton'
}
</script>
<style scoped>
.button {
  margin-bottom: 40px
}
</style>