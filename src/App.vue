<template>
<intro />
<lesson-two />
</template>

<script>
import Intro from './components/Intro.vue'
import LessonTwo from './components/lessonTwo.vue'


export default {
  components: { Intro, LessonTwo },
  name: 'App'
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
 
}
</style>
