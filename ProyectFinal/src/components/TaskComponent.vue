<script setup>
const props = defineProps(
    {
        tarea: {
            type: String,
            default: 'Tarea por defecto'
        },
        index: {
            type: Number
        }
    }
)

const emit = defineEmits(['borrarHijo'])

function borrar(index){
    // console.log('borrar hijo', index)
    emit('borrarHijo', index)
}
</script>

<template>
    <div class="flex justify-between px-4 py-1 bg-gray-200 rounded mt-2">
        {{ props.tarea }}
        <span 
        @click="borrar(props.index)"
        class="transition-colors duration-500 hover:cursor-pointer hover:bg-red-800 px-2 text-center text-white bg-red-600 rounded ">
        X
    </span>
    </div>

</template>