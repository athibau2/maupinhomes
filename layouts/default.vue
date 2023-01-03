<template>
  <v-app>
    <v-app-bar
      height="90px"
      fixed
      absolute
      app
      flat
      color="transparent"
      src="~/assets/images/projects/crops/pic5.jpg"
    >
      <!-- <img src="~/assets/images/projects/crops/pic5.jpg" width="100%" /> -->
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, #edf0ee, #9c8c94"
        ></v-img>
      </template>
      <img src="~/assets/images/maupin_homes_logo-hq.png" width="120px" />
      <!-- <v-toolbar-title>{{ title }}</v-toolbar-title> -->
      <v-spacer />
      <v-btn class="nav-btn"
        elevation="0"
        color="transparent"
        height="50px"
      >
        Gallery
      </v-btn>
      <v-btn class="nav-btn"
        elevation="0"
        color="transparent"
        height="50px"
      >
        Reviews
      </v-btn>
      <v-btn class="nav-btn"
        elevation="0"
        color="transparent"
        height="50px"
      >
        Contact Us
      </v-btn>
      <!-- <v-app-bar-nav-icon /> -->
    </v-app-bar>
    <v-main class="main">
      <!-- <v-container> -->
        <Nuxt />
      <!-- </v-container> -->
    </v-main>
    <v-footer
      absolute
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Maupin Homes LLC'
    }
  }
}
</script>

<style scoped>
@import "~/assets/styles.css";

.nav-btn {
  /* margin-right: 5px; */
  font-size: 15px;
  color: #2c2924;
}

</style>
