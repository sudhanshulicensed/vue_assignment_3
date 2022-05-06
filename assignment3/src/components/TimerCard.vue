<template>
    <div class="timer-card" @isClicked="interVal" :timeVal="interValue">
        <TimerDisplay :timer="count"/>
        <ControlButton @isStarted="timerStarted" @isStopped="timerClosed" />
    </div>
</template>

<script>

import TimerDisplay from "./CountDisplay.vue"
import ControlButton from "./Control.vue"

export default {
    props: {
        timer: {
            type: Number,
            default: 0,
        }
    },
    name: "TimerCard",
    components: {
        TimerDisplay,
        ControlButton,
    },
    data() {
        return {
            name: "0",
            interValue: null,
            count: 0,
            clear: null,
        }
    },
    methods: {
        increaseCount() {
            this.count++;
            console.log(this.count)
        },
        interVal(val) {
            this.interValue = val;
        },
        timerStarted() {
            this.close = setInterval(this.increaseCount, 1000)
        },
        timerClosed() {
            clearInterval(this.close);
            this.count = 0;
        },
    }
}
</script>

<style>
    .timer-card{
        box-sizing: border-box;
        width: 200px;
        height: 100px;
        background-color: rgba(248, 239, 186, 0.8);
        border-radius: 5px;
        padding: 1%;
        margin-bottom: 5px;
        margin-right: 5px;
    }
</style>