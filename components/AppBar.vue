<template>
  <nav>
    <v-app-bar
      :clipped-left="clipped.val"
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer.val = !drawer.val" />
      <v-btn
        icon
        @click.stop="miniVariant.val = !miniVariant.val"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant.val ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="clipped.val = !clipped.val"
      >
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="fixed.val = !fixed.val"
      >
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn
        icon
        @click.stop="rightDrawer.val = !rightDrawer.val"
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
  </nav>
</template>

<script>
export default {
  props: {
    drawer: {
      type: Object,
      default:()=> {val: false}
    },
    rightDrawer: {
      type: Object,
      default:()=> {val: false}
    },
    miniVariant: {
      type: Object,
      default:()=> {val: false}
    },
    clipped: {
      type: Object,
      default:()=> {val: false}
    },
    fixed: {
      type: Object,
      default:()=> {val: false}
    },
    title: String
  },
  data () {
    return {
      right: true,
    }
  },
}
</script>
