<template>
  <nav>
    <v-app-bar app class="blue-grey lighten-1">
      <v-app-bar-nav-icon v-on:click="clickDrawer"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <span class="font-weight-black">SOUNDBOARD</span><span class="font-weight-light">APP</span>
      </v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer app class="blue-grey lighten-1" v-model="isDrawerOpen">
      <v-list nav>

        <v-list-item v-on:click="navigate('/')">
          <v-list-item-icon>
            <v-icon>home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Home</v-list-item-title>
        </v-list-item>

        <v-list-item v-on:click="navigate('about')">
          <v-list-item-icon>
            <v-icon>info</v-icon>
          </v-list-item-icon>
          <v-list-item-title>About Us</v-list-item-title>
        </v-list-item>

        <v-list-item v-on:click="navigate('support')">
          <v-list-item-icon>
            <v-icon>live_help</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Support</v-list-item-title>
        </v-list-item>

      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isDrawerOpen: false
    }
  },
  methods: {
    clickDrawer() {
      this.isDrawerOpen = true;
    },
    navigate(navi) {
      this.$router.push(navi);
    }
  }
}
</script>

<style>

</style>