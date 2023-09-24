<template>
  <div class="card text-left mt-2">
    <div class="card-body text-center">
        <h4 class="card-title">Life cycle hook</h4>
        
    </div>
  </div>
</template>

<script>
import { onBeforeMount, onMounted } from 'vue';

export default {
    setup(){
        console.log("before-create - Created");
        onBeforeMount(function(){
            console.log("on-before-create-mount");
        });
        onMounted(function(){
            console.log("on-mounted");
        });
    },
    
}
</script>

<style>

</style>