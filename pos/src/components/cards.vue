<template>
<div>
    <div v-for="category in categories" :key="category">
        <h2 style="margin-left: 95px;">{{ category }}</h2>
  <v-container fluid> 
    <v-slide-group
      v-model="model"
      class="pa-4"
      center-active
      show-arrows
    >
      <v-slide-item
        v-for="n in products.length"
        :key="n"
        v-slot="{ active, toggle }"
      >
        <v-card
          :color="active ? 'grey lighten-1' : 'white'"
          class="ma-4"
          height="330"
          width="300"
          @click="toggle"
        >
        
        <v-img
          height="150"
          src='https://cdn.vuetifyjs.com/images/cards/cooking.png'
          cover
          ></v-img>

          <v-card-header>
      <div align="center">
      <v-card-header-text>
        <div style="height: 25px">
        <v-card-subtitle>Cras id posuere (Optio)</v-card-subtitle>
        </div>
        <div style="height: 45px">
        <v-card-title class="justify-center" >
          <span class="mr-1">$0.0</span>
        </v-card-title >
        </div>
        
        <v-card-actions class="justify-center">
          <div>
          <v-btn>
            <span>Add to Cart</span>
          </v-btn>
          <hr style="height: 15px; visibility: hidden">
          <v-btn color="white">
            <span class="red--text">Buy Now</span>
          </v-btn>
        </div>
        </v-card-actions>
        
      </v-card-header-text>
      </div>
    </v-card-header>
        
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <!-- <v-scale-transition>
              <v-icon
                v-if="active"
                color="white"
                size="48"
                v-text="'mdi-close-circle-outline'"
              ></v-icon>
            </v-scale-transition>  -->
          </v-row>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-container>
        </div>
</div>
</template>

<script>
export default {
    name: 'myCards',
    data: () => ({
        categories: [
        'Lorem ipsum',
        'Aspernatur',
        'Consequatur',
        'Itaque earum',
        'Nam libero tempore',
        'Voluptate velit',
        'Officiis debitis',
      ],
      products: [
        { title: 'Libero tempore', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', unit: "Litora", price: "0.0"},
        { title: 'Officiis debitis', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', unit: "Augue"},
        { title: 'Itaque earum', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', unit: "Class" },
        { title: 'Donec pharetra', src: 'https://cdn.vuetifyjs.com/images/cards/cooking.png', unit: "Sed" },
        { title: 'Libero tempore', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', unit: "Litora", price: "0.0"},
        { title: 'Officiis debitis', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', unit: "Augue"},
        { title: 'Itaque earum', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', unit: "Class" },
        { title: 'Donec pharetra', src: 'https://cdn.vuetifyjs.com/images/cards/cooking.png', unit: "Sed" },
        { title: 'Libero tempore', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', unit: "Litora", price: "0.0"},
        { title: 'Officiis debitis', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', unit: "Augue"},
        { title: 'Itaque earum', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', unit: "Class" },
        { title: 'Donec pharetra', src: 'https://cdn.vuetifyjs.com/images/cards/cooking.png', unit: "Sed" }
      ]
    }),
    }
</script>