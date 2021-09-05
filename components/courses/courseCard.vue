<template>
  <NuxtLink :to="link" tag="div" style="cursor: pointer">
    <v-card class="course-card" max-width="500">
      <v-container>
        <v-row class="mt-0" justify="center">
          <h1 :style="'color:' + color">{{ name }}</h1>
        </v-row>
        <v-row class="pt-2 pb-6" justify="center">
          <v-img
            max-width="100"
            max-height="80"
            contain
            :src="require('~/assets/images/langs/' + image)"
          >
          </v-img>
        </v-row>
      </v-container>
    </v-card>
  </NuxtLink>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      default: 'Language',
    },
    color: {
      type: String,
      default: '#eee',
    },
    image: {
      type: String,
      default: '',
    },
    link: {
      type: String,
      default: '',
    },
  },
}
</script>
<style lang="scss" scoped>
.course-card {
  background-color: $c-dark !important;
}
</style>
