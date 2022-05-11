<template>
  <div :style="container">
    <p
      :style="{
        color: `rgb(233, 101, 178)`,
        fontSize: '30px',
        fontWeight: '700',
        lineHeight: '10px',
      }"
    >
      <span :style="{ color: 'rgb(5, 153, 5)' }">Vue.js</span> 👍 : Lesson 2
    </p>
    <p v-show="showElement">You are seeing this because v-show is TRUE!</p>
    <p>Btw, here are my technical skills :</p>
    <div :style="{display:'grid', gridTemplateColumns:'1fr 1fr 1fr'}" v-show="showSkills">
        <p v-for="(skill, index) in skills" :key="index" :style="{color: 'rgb(52, 167, 206)'}"> {{skill.name}}</p>
    </div>
    <button @click="toggle" :style="{
        background:'orange',
        border:'none',
        color:'#fff',
        padding:'10px 15px',
        borderRadius:'5px',
        marginTop:'20px',
        cursor:'pointer'
    }">Show/Hide skills</button>
         <p class="sectionOverView">In this section, i learnt conditional rendering, list rendering, list & keys, conditional list rendering and Methods 💃🏽</p>
  </div>

</template>
<script>

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "LessonTwo",
  data() {
    return {
      showElement: true,
      showSkills: true,
      container: {
        width: "90%",
        border: "1px solid lightBlue",
        margin: "60px auto 0",
        padding: "30px 0",
      },
      skills: [
          {
              name: 'HTML'
          },
           {
              name: 'CSS'
          },
           {
              name: 'Javascript'
          },
           {
              name: 'Typescript'
          },
           {
              name: 'Tailwind'
          },
           {
              name: 'React.js'
          },
           {
              name: 'Next.js'
          },
           {
              name: 'Styled Components'
          },
           {
              name: 'SCSS/SASS'
          }
      ]
    };
  },
  methods: {
      toggle(){
          this.showSkills = !this.showSkills
      }
  }
};
</script>

<style>
.sectionOverView {
  font-size: 12px;
  font-style: italic;
  margin-top: 40px;
}
</style>
