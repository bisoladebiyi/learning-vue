<template>
  <div :style="container">
    <p
      :style="{
        color: 'magenta',
        fontSize: '30px',
        fontWeight: '700',
        lineHeight: '10px',
      }"
    >
      <span :style="{ color: 'rgb(5, 153, 5)' }">Vue.js</span> 👍 : Lesson 3
    </p>
    <p>
      When i click on the button, the button value shall appear : {{ btnValue }}
    </p>
    <button
      @click="getValue"
      value="Hey there! I am Value"
      :style="{
        background: 'orange',
        border: 'none',
        color: '#fff',
        padding: '10px 15px',
        borderRadius: '5px',
        marginTop: '20px',
        cursor: 'pointer',
      }"
    >
      Click me
    </button>
    <div>
      <p>Your name is : {{formVal.name}} </p>
      <p>You are : {{formVal.age}} : years old</p>
      <p>You're a : {{formVal.occupation}}</p>
    </div>

    <form action="" :style="{textAlign:'left', width:'50%', margin:'0 auto'}">
      <div>
        <label for="" :style="{display:'block'}">Name</label>
        <input :style="{width:'100%', padding:'6px 10px'}" type="text" v-model="formVal.name" />
      </div>
        <div :style="{marginTop:'20px'}">
        <label for="" :style="{display:'block'}">Age</label>
        <input :style="{width:'100%', padding:'6px 10px'}" type="text" v-model="formVal.age" />
      </div>
        <div :style="{marginTop:'20px'}">
        <label for="" :style="{display:'block'}">Occupation</label>
        <input :style="{width:'100%', padding:'6px 10px'}" type="text" v-model="formVal.occupation" />
      </div>
  
    </form>
    <p class="sectionOverView">
      In this section, i learnt event and form handling 💃🏽
    </p>
  </div>
</template>
<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "LessonThree",
  data() {
    return {
      container: {
        width: "90%",
        border: "1px solid lightBlue",
        margin: "60px auto 0",
        padding: "30px 0",
      },
      btnValue: "",
      formVal: {
        name:"",
        age:"",
        occupation:""
      }
    };
  },
  methods: {
    getValue(e) {
      this.btnValue = e.target.value;
    },
  },
};
</script>

<style>
.sectionOverView {
  font-size: 12px;
  font-style: italic;
  margin-top: 40px;
}
</style>
