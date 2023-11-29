<script setup>
import { ref } from 'vue';

let accept = ref(true)

function si(){
  alert("Mi niña yo sabia que si querias ser mi novia ❤")
}
function no(){
  accept.value = false
  
}
function si2(){
  accept.value = true
}
</script>

<template>
  <div class="container">
    <div>
      <h1>¿Quieres ser mi novia?</h1>
    </div>
    <div class="button">
      <div class="button1" @click="si" v-show="si" v-if="accept">¿Sí?</div>
      <div class="button2" @click="no"  v-if="accept" >¿No?</div>
      <div class="button1" @click="si2" v-if="!accept">¿No?</div>
      <div class="button1" @click="si2" v-if="!accept">¿Sí?</div>
    </div>
  </div>
</template>

<style scoped>
h1{
  text-align: center;
}
.button2{
  background-color: #7A577A;
  border-radius: 4px;
  padding: 5px 5px;
  cursor: pointer;
}
.button1{
  background-color: #7A577A;
  border-radius: 4px;
  padding: 5px 5px;
  cursor: pointer;
}
.button{
  background-color: #F2E3D5;
  border-radius: 4px;
  display: flex;
  justify-content: space-around;
  padding: 10px;
}
.container{
  padding: 6px 6px;
  background-color: #89D99D;
  max-width: 420px;
  margin: 0 auto;
  font-family: 'Edu TAS Beginner', cursive;
  margin-top: 20%;
  border-radius: 4px;
  color: white;
}

</style>
