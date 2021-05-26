<template>
  <div>
  <v-card
    color="grey lighten-4"
    flat
   
    tile
  >
    <v-toolbar color="indigo" dense dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text>
        About
      </v-btn>
      <v-btn text>
        Contact us
      </v-btn>
      <v-btn text>
        Login
      </v-btn>
    </v-toolbar>
  </v-card>
 <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
  <v-container>
  <v-subheader>Grid system</v-subheader>
    <v-row>
    <v-col>
    <v-card>
      This is card 1 
    </v-card>
    </v-col>
    <v-col>
    <v-card>
      This is card 2 
    </v-card>
    </v-col>
    <v-col>
    <v-card>
      This is card 3
    </v-card>
    </v-col>
    </v-row>
    <v-spacer/>
    <v-row>
    <v-col cols="8">
    <v-card>
      This is the first card 
    </v-card>
    </v-col>
    <v-col cols="4">
    <v-card>
      This is the second card
    </v-card>
    </v-col>
 </v-row>

  </v-container>		
 <v-footer
    dark
   padless>
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>
      <v-divider></v-divider>
      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
  </div>
</template>
<script>
// @ is an alias to /src
export default {
  name: 'Home',
    data: () => ({
              items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
     
    icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>
