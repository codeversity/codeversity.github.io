<template>
  <div>
    <v-row justify="center">
      <h1 class="mt-8">Pick your poison</h1>
    </v-row>
    <v-row justify="center">
      <v-col
        v-for="language in languages"
        :key="language.name"
        cols="12"
        md="6"
        lg="3"
        align="center"
      >
        <course-card
          :name="language.name"
          :color="language.color"
          :image="language.image"
          :link="language.link"
        />
      </v-col>
    </v-row>
  </div>
</template>
<script>
import courseCard from '~/components/courses/courseCard.vue'

export default {
  components: { courseCard },
  data() {
    return {
      languages: [
        {
          name: 'HTML',
          color: '#e56027',
          image: 'html5.png',
          link: 'html',
        },
        {
          name: 'CSS',
          color: '#264de4',
          image: 'css3.png',
          link: 'css',
        },
        {
          name: 'JavaScript',
          color: '#f7e018',
          image: 'js.png',
          link: 'js',
        },
        {
          name: 'Python',
          color: '#ffd03c',
          image: 'py.png',
          link: 'python',
        },
        {
          name: 'C#',
          color: '#9a4993',
          image: 'csharp.png',
          link: 'csharp',
        },
        {
          name: 'Java',
          color: '#e76f00',
          image: 'java.png',
          link: 'java',
        },
        {
          name: 'C',
          color: '#5d6cbf',
          image: 'c.png',
          link: 'c',
        },
        {
          name: 'C++',
          color: '#659bd3',
          image: 'cpp.png',
          link: 'cpp',
        },
      ],
    }
  },
}
</script>
