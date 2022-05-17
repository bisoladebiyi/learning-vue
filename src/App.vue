<template>
<intro />
<lesson-two />
<lesson-three />
</template>

<script>
import Intro from './components/Intro.vue'
import LessonThree from './components/lessonThree.vue'
import LessonTwo from './components/lessonTwo.vue'


export default {
  components: { Intro, LessonTwo, LessonThree },
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
