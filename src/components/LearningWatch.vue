<template>
  <div class="card text-left mt-2">
    <div class="card-body text-center">
        <h4 class="card-title">Watch</h4>
        
        <p class="badge badge-info">Count: {{count}}</p>
        <div><button class="btn btn-danger" @click="handleIncreasementCount">Increasement Count</button></div>
    </div>
  </div>
</template>

<script>
import { ref,watch } from 'vue'
export default {
    setup(){
        const count = ref(1);
        function handleIncreasementCount(){
            count.value +=1;
        }
        watch(count,function(newValue, oldValue){
            console.log(newValue, oldValue);
            if(newValue > 10){
                count.value = 1;
            }
        });
        return {
            count : count,
            handleIncreasementCount,
        };
    }
}
</script>

<style>

</style>