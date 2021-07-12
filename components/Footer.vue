<template>
  <nav>
    <v-footer
      :absolute="!fixed.val"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>

  </nav>
</template>

<script>
export default {
  props: {
    fixed: {
      type: Object,
      default:()=> {val: false}
    },
  }
}
</script>
