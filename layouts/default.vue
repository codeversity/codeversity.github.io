<template>
  <v-app class="bg">
    <v-main>
      <navbar />
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import navbar from '~/components/navbar.vue'
export default {
  components: { navbar },
}
</script>
<style lang="scss" scoped>
.bg {
  background-color: $c-bg;
}
</style>
