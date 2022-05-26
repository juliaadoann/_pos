<template>
    <div>
      <v-container class="toolbar">
        <v-row>
    <v-col
      cols="12"
      sm="6"
      md="10"
    >
        <v-chip-group
          mandatory
          active-class="primary--text"
          >
            <v-chip
            class="ma-2"
              v-for="tag in tags"
              :key="tag"
            >
              {{ tag }}
            </v-chip>
        </v-chip-group>
        </v-col>
        <v-col
        cols="12"
        sm="6"
        md="2">
        <v-text-field
        label="Search items"
        outlined
        dense
        prepend-inner-icon="mdi-magnify"></v-text-field>
        </v-col>
        </v-row>
  </v-container>
  </div>
</template>

<script>
export default {
    name:'myChips',
    data: () => ({
        tags: [
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
        'Textos',
        'Contrario',
        'Contenido',
        'Sólo',
        'Esencialmente',
        'Phasellus',
      ]
    })
}
</script>
<style scoped>
.toolbar {
  margin-left: 20px
}
</style>