<template>
  <nav>
    <v-navigation-drawer
      v-model="drawer.val"
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  props: {
    drawer: {
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
    items: Array,
  },
  data () {
    return {
    }
  },
}
</script>
