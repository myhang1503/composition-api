<template>
  <div class="card text-left mt-2">
    <div class="card-body text-center">
        <h4 class="card-title">Computed</h4>
        <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Firstname" aria-label="Firstname" v-model="firstName">
            <span class="input-group-text">@</span>
            <input type="text" class="form-control" placeholder="Lastname" aria-label="Lastname" v-model="lastName">
        </div>
        <p class="badge badge-info">Họ và tên: {{fullName}}</p>
    </div>
  </div>
</template>

<script>
import { computed, ref} from "vue";
export default {
    setup(){
        const firstName = ref(""); //get from v-model
        const lastName = ref("");

        function setFirstName(event){ //for @input = "setFirstName"
            firstName.value = event.target.value;
        }
        function setLastName(event){ //for @input = "setLastName"
            lastName.value = event.target.value;
        }
        //computed
        const fullName = computed(() => firstName.value + " " + lastName.value);

        return{
            firstName, //firstName : firstName
            lastName,
            setFirstName,
            setLastName,
            fullName
        };
    },
}
</script>

<style>

</style>