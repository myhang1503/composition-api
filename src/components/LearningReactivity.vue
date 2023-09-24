<template>
  <div class="card text-left">
    <div class="card-body text-center">
      <h4 class="card-title">Reactivity</h4>
      <p class="card-text">{{user.name}}</p>
      <p class="card-text">{{user.age}}</p>
    </div>
  </div>
</template>

<script>
import {isReactive, isRef, reactive, ref} from "vue";
export default {
  // data: function(){
  //   return{
  //     name: "Ng Phong Hào",
  //   }
  // },
  // created(){
  //   setTimeout(() => {
  //     this.name = "Sweetdream";
  //   }, 2000);
  // }
  setup(){
    let userName = ref("Ng Phong Hào");
    let user = reactive({
      name: "Ng Phong Hào",
      age: 23
    });
    setTimeout(()=>{
      userName.value = "Sweetdream";
      user.name = "Sweetdream";
      user.age = 22;

    }, 2000);

    console.log(isRef(userName)); //check kha nang reactive
    console.log(isReactive(user)); //check kha nang reactive

    return{
      userName,
      user,
    };
  },
  
}
</script>

<style>

</style>