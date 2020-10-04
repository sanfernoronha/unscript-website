<template>
  <v-app>
    <v-app-bar app flat dark height="100" id="top">
      <div class="d-flex align-center">
        <v-img
          alt="Unscript Logo"
          class="shrink mr-2"
          contain
          src="./assets/unscript.png"
          transition="scale-transition"
          width="70"
        />
      </div>

      <v-spacer></v-spacer>
      <v-app-bar-nav-icon large class="hidden-md-and-up" @click.stop="drawer = !drawer" />
      <v-btn
        outlined
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
        class="hidden-sm-and-down mr-2"
      >HOME</v-btn>
      <v-btn
        outlined
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
        class="hidden-sm-and-down mr-2"
      >ABOUT</v-btn>
      <v-btn
        outlined
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
        class="hidden-sm-and-down mr-2"
      >DOMAINS</v-btn>
      <v-btn
        outlined
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
        class="hidden-sm-and-down mr-2"
      >SCHEDULE</v-btn>
      <v-btn
        outlined
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
        class="hidden-sm-and-down mr-2"
      >SPONSORS</v-btn>
      <v-btn
        outlined
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
        class="hidden-sm-and-down mr-2"
      >FAQS</v-btn>
    </v-app-bar>
    <!-- Drawer -->
    <v-navigation-drawer
      v-model="drawer"
      absolute
      left
      temporary
      class="hidden-md-and-up"
      style="position:fixed;top:0;left:0;overflow-y:scroll;"
    >
      <v-list nav shaped>
        <v-list-item-group active-class="deep-purple--text text--accent-4" v-model="group">
          <v-list-item @click="$vuetify.goTo('#about',options)">
            <v-list-item-title>About</v-list-item-title>
          </v-list-item>

          <v-list-item @click="$vuetify.goTo('#schedule',options)">
            <v-list-item-title>Schedule</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-content>
      <HelloWorld />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld
  },

  data: () => ({
    drawer: false,
    group: null,
    duration: 600,
    offset: -2000,
    easing: "easeInOutCubic"
  }),
  methods: {
    options() {
      return {
        duration: 600,
        offset: -500,
        easing: this.easing
      };
    }
  },
  watch: {
    group() {
      this.drawer = false;
    }
  }
};
</script>
