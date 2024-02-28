
<template>
    <div class="home">
        <h3>{{ counterData.title }}:</h3>
        <div class="counterBtn">
            <button @click="decrementCounter(2)" class="button">--</button>
            <button @click="decrementCounter(1)" class="button">-</button>
            <span class="counter">{{ counterData.count }}</span>
            <button @click="incrementCounter(1, $event)" class="button">+</button>
            <button @click="incrementCounter(2)" class="button">++</button>

        </div>
        <div class="edit">
            <h4>Edit counter title</h4>
            <input v-model="counterData.title" type="text">
        </div>
        <p>the number {{ itsOdd }}</p>
    </div>
</template>

<script setup>
import { reactive, computed, watch} from 'vue';

//object reactive queremos guardar todo en un objeto tanto nuestro counter como nuestro titulo
// const counter = ref(0)
// const counterTitle = ref('My counter')

const counterData = reactive({
    count: 0,
    title: 'My counter'
})

watch(() => {
    if (counterData.count === 20) alert('This is number has reached 20')
})

const itsOdd = computed(() => {
    if( counterData.count % 2 === 0) {
        return ' is even'
    } return 'is odd'
});

const incrementCounter = (amount, event) => {
    console.log(amount)
    console.log(event)
    counterData.count += amount;
}

const decrementCounter = (amountRes) => {
    counterData.count -= amountRes
}
</script>

<style scoped>
.home{
    font-size: 48px;
    text-align: center;
}
.counterBtn{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
}
.button, .counter{
    font-size: 40px;
    margin: 10px;
}
.edit{
    margin-top: 30px;
}


</style>