<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" app temporary>
      <v-list dense nav>
        <v-subheader class="text-uppercase font-weight-bold">
          Menu
        </v-subheader>
        <v-list-item v-for="(item, index) in routes" :key="index" :to="item.link">
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-btn
      class="d-md-none drawer-button"
      rounded
      @click="drawer = !drawer"
    >
      <v-icon right>
        mdi-menu
      </v-icon>
    </v-btn>

    <v-app-bar app height="80">
      <v-app-bar-nav-icon class="d-md-none" @click="drawer = !drawer" />
      <v-container class="py-0 px-0 px-sm-2 fill-height">
        <nuxt-link to="/" class="d-flex align-center text-decoration-none mr-2">
          <img src="/images/logo.png" alt="" height="48" class="mr-1">
          <span class="font-weight-black text-uppercase text-h5 ml-1">
            ParagonX <span class="white--text">Academy</span>
          </span>
        </nuxt-link>

        <v-spacer />
        <div class="d-none d-md-block">
          <v-btn
            v-for="(item, index) in routes"
            :key="index"
            text
            :to="item.link"
            class="mx-1"
          >
            {{ item.title }}
          </v-btn>
        </div>
      </v-container>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      routes: [
        {
          link: '/',
          title: 'Home'
        },
        {
          link: '/events',
          title: 'Events'
        },
        {
          link: '/about',
          title: 'About'
        }
      ],
      drawer: false
    }
  }
}
</script>
