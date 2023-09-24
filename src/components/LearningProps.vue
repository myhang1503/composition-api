<template>
  <div class="card text-left mt-2">
    <div class="card-body text-center">
      <h4 class="card-title">Props</h4>
      <img :src="image" class="img-thumbnail"/>
    </div>
  </div>
</template>

<script>
import { toRefs } from 'vue';
export default {
  props:{
    image:{
      type: String,
      required: true,
      default: "default.jpg",
    },
  },
  // methods:{
  //   getImage(){
  //     console.log(this.image)
  //   },
  // },
  setup(props){
    const {image} = toRefs(props);
    console.log(image);
  },
};
</script>

<style>

</style>