<template>
  <nav>
    <v-navigation-drawer
      v-model="drawer.val"
      :right="right"
      v-bind="$attrs"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
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
  },
  data () {
    return {
      right: true,
    }
  },
}
</script>
