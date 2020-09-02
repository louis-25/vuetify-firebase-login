<template>
    <v-app>
        <v-app-bar app="app" color="primary" dark="dark">
            <v-app-bar-nav-icon @click="drawer = !drawer"/>
            <site-title :title="title"></site-title>
            <v-spacer></v-spacer>
            <site-btn></site-btn>
        </v-app-bar>
        <v-content>
          <v-navigation-drawer app="app" v-model="drawer">
            <site-drawer></site-drawer>
            </v-navigation-drawer>
            <router-view/>
        </v-content>
        <site-footer :footer="footer"></site-footer>
    </v-app>
</template>

<script>
import SiteTitle from '@/views/site/title'
import SiteFooter from '@/views/site/footer'
import SiteDrawer from '@/views/site/drawer'
import SiteBtn from '@/views/site/app-bar-btn'

export default {
  components: {
    SiteTitle,
    SiteFooter,
    SiteDrawer,
    SiteBtn
  },
  name: 'App',
  data () {
    return {
      drawer: false,
      title: 'Welcome',
      footer: 'IMNUGU'
    }
  }
}
</script>
