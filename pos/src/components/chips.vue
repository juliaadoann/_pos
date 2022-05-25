<template>
    <div>
      <v-container style="margin-left: 20px">
        <v-row>
    <v-col
      cols="10"
      sm="10"
      md="10"
    >
      
        <v-chip-group
          mandatory
          active-class="primary--text">
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
        cols="2"
        sm="2"
        md="2">
        <v-autocomplete
              v-model="values"
              outlined
              dense
              label="Lorem ipsum"></v-autocomplete>
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