<script setup>
import { ref, computed, defineProps, inject, watch} from 'vue';

const user = inject("userName",null)

const props = defineProps({
    var1: String,
    var2: String,
})


const firstName = ref('Yair');
const lastName = ref('Chira');

const otherName = `${props.var1} ${props.var2}`

const fullName = computed(() => {
    return `${firstName.value} ${lastName.value }`
});

const btn = ref(null);
watch(btn, (valor) => {

    console.log(valor);
})

//        USO DE REF()
// const dataCounter = ref({
//     counter: 0,
// });
//        USO DE REACTIVE()
// const dataCounterReactive = reactive({
//     counter: 0,
// });


//setInterval(() => dataCounter.value.counter++, 5000);
//setInterval(() => dataCounterReactive.counter++, 5000);


//        USO DE WATCH
// watch(() => dataCounterReactive.counter,
//         ( valor, anterior) => {
//             console.log(valor, anterior)
//         })
// Con el uso de ref
//   const count = ref(0)
//   watch(count, (count, prevCount) => {
//      console.log(count, prevCount)
// })
</script>


<template>
    <div>
        {{ fullName }} {{ otherName }} {{ user }}
    </div>
    <button ref="btn">Click</button>


    <!-- <p>{{ dataCounterReactive.counter }}</p> -->
</template>
