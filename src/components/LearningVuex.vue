<template>
  <div class="card text-left mt-2">
    <div class="card-body text-center">
        <h4 class="card-title">Vuex</h4>
        
        <p class="badge badge-info">Count: {{count}}</p>
        <div><button class="btn btn-danger" @click="increamentCount">Increasement Count</button></div>
    </div>
  </div>
</template>

<script>
import { computed } from 'vue';
import {useStore} from 'vuex'
export default {
    setup(){
        //this.$store => store
        const store = useStore();
        const count = computed(()=>store.state.count);
        function increamentCount(){
            store.dispatch("incrementAction");
        }
        return{
            count,
            increamentCount
        }
    }
}
</script>

<style>

</style>