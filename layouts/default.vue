<template>
  <Facade>
    <template v-slot:main>
      <v-container>
        <Nuxt />
      </v-container>
    </template>
  </Facade>
</template>

<script>
import Facade from '/components/Facade.vue'

export default {
  components: {Facade}
}
</script>
