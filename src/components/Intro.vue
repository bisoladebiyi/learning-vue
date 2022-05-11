<template>
<div :style="container">
    <p :style="{
        color: `lightPink`,
        fontSize: '30px',
        fontWeight: '700',
        lineHeight: '10px'
    }"><span :style="{color: 'rgb(5, 153, 5)'}">Vue.js</span> 👍 : Lesson 1</p>
<div>Hello there</div>
<img :src="myImg" :class="imgStyle" alt="">
    <p :class="col">{{name}}, a {{ role }}</p>
    <div v-html="hack" :class="link"></div>
    <p class="sectionOverView">In this section, i learnt about Vue as a js framework, creating a vue app, templates, single file components and binding (binding text, binding html, binding attributes and binding classes!) 💃🏽</p>
</div>
    
</template>
<script>

import me from '../assets/IMG_2037.jpg'
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Intro',
 data(){
   return {
    myImg:me,
    name: "I'm Bee",
    role: "Frontend engineer",
    hack: `<a onclick="alert('hii, im new to Vue')">click here for a surprise</a>`,
    col: 'newColor',
    bool: true,
    link:'link',
    imgStyle:"img",
    container: {
        width:'90%',
        border:'1px solid lightgreen',
        margin: '0 auto',
        padding: '30px 0'
    }
   }
   
 }
}
</script>

<style>
.newColor {
    color: rgb(52, 167, 206);
}.link{
    color: rgb(5, 153, 5);
    cursor: pointer;
    font-weight: 700;
    font-size: 20px;
}.sectionOverView{
    font-size: 12px;
    font-style: italic;
    margin-top: 40px;
}.img{
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    margin-top: 10px;
    border: 10px solid rgb(233, 200, 101);
}
</style>