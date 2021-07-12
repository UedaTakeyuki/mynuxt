<template>
  <v-app dark>
    <NavDraw
      :drawer="drawer"
      :items="items"
      :miniVariant="miniVariant"
      :clipped="clipped"
    />
    <AppBar
      :drawer="drawer"
      :rightDrawer="rightDrawer"
      :clipped="clipped"
      :miniVariant="miniVariant"
      :title="title"
      :fixed="fixed"
    />
    <v-main>
      <slot name="main">
        <v-container>
          <Nuxt />
        </v-container>
      </slot>
    </v-main>
    <RNavDraw
      :drawer="rightDrawer"
    />
    <Footer
      :fixed="fixed"
    />
  </v-app>
</template>

<script>
  import NavDraw from '/components/NavDraw.vue'
  import RNavDraw from '/components/RNavDraw.vue'
  import AppBar from '/components/AppBar.vue'
  import Footer from '/components/Footer.vue'

  export default {
    components: {
      NavDraw,
      RNavDraw,
      AppBar,
      Footer
    },
    data () {
      return {
        clipped: {val: false},
        drawer: {val: false},
        fixed: {val: false},
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
        miniVariant: {val: false},
        rightDrawer: {val: false},
        title: 'Vuetify.js'
      }
    }
  }
</script>
