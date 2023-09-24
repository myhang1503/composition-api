<template>
  <div class="card text-left">
    <div class="card-body text-center">
      <h4 class="card-title">Method</h4>
      <p class="card-text">{{user.name}}</p>
      <p class="card-text">{{user.age}}</p>
      <button class="btn btn-success" @click="handleClick">Change</button>
    </div>
  </div>
</template>

<script>
import { reactive, ref} from "vue";
export default {
  setup(){
    let userName = ref("Ng Phong Hào");
    let user = reactive({
      name: "Ng Phong Hào",
      age: 23
    });

    // function handleClick(){
    //     userName.value = "Sweetdream";
    //     user.name = "Sweetdream";
    //     user.age = 22;
    // }

    //thuong dung trong truong hop co tu khoa this, nen dung function bthg
    const handleClick = () => {
        userName.value = "Sweetdream";
        user.name = "Sweetdream";
        user.age = 22;
    }

    return{
      userName,
      user,
      handleClick,
    };
  },
  
}
</script>

<style>

</style>