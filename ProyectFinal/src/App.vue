<script setup>
import TaskComponent from '@/components/TaskComponent.vue';
import { ref } from 'vue';

const tareas = ref(['Ninguna', 'Un Bladimir', 'Dormir'])

function deleteTask(index){
  tareas.value.splice(index, 1)
}
</script>

<template>
  <div class="w-96 bg-gray-300 shadow-md rounded mx-auto px-4 py-2 mt-12">
    <h1 class=" text-2xl font-semibold text-center ">List of Tasks</h1>

    <div class="flex mt-2">
      <input type="text" 
      class="outline-none rounded-r-none w-4/5 h-8 px-2 py-1 border border-green-600 rounded"
      >
      <span class="transition-colors duration-500 hover:cursor-pointer hover:bg-green-800 rounded-l-none w-1/5 h-8 text-xl font-bold text-center text-white bg-green-600 rounded ">
        +
      </span>
    </div>

    <TaskComponent 
      v-for="(tarea, index) in tareas"
      :key="index"
      :tarea="tarea"
      :index="index"
      @borrarHijo="deleteTask"
    />
    <!-- <task-component /> -->
    
  </div>
</template>
