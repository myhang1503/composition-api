<template>
  <main class="container">
    <img alt="Vue logo" src="./assets/logo.png">
    <learning-reactivity></learning-reactivity>
    <learning-props image="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRoul62ksKjjX0kyxbri42A5dEvwXybsqh7Rw&usqp=CAU"></learning-props>
    <learning-method image="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRoul62ksKjjX0kyxbri42A5dEvwXybsqh7Rw&usqp=CAU"></learning-method>
    <learning-computed></learning-computed>
    <learning-watch></learning-watch>
    <learning-ref-template></learning-ref-template>
    <learning-provide-inject></learning-provide-inject>
    <learning-life-cycle-hook></learning-life-cycle-hook>
    <learning-vuex-vue></learning-vuex-vue>
  </main>
</template>

<script>
import LearningComputed from './components/LearningComputed.vue'
import LearningMethod from './components/LearningMethod.vue'
import LearningProps from './components/LearningProps.vue'
import LearningProvideInject from './components/LearningProvideInject.vue'
import LearningReactivity from './components/LearningReactivity.vue'
import LearningRefTemplate from './components/LearningRefTemplate.vue'
import LearningWatch from './components/LearningWatch.vue'
import LearningLifeCycleHook from './components/LearningLifeCycleHook.vue'
import LearningVuexVue from './components/LearningVuex.vue'

import {provide,ref} from "vue";


export default {
  name: 'App',
  components: {
    LearningReactivity,
    LearningProps,
    LearningMethod,
    LearningComputed,
    LearningWatch,
    LearningRefTemplate,
    LearningProvideInject,
    LearningLifeCycleHook,
    LearningVuexVue
  },
  setup(){
    const age = ref(1);
    setInterval(() => {
      age.value += 1;
    }, 5000);
    provide("name","sweetdream");
    provide("age",age);
  }
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
