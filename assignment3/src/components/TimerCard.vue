<template>
    <div class="timer-card" @isClicked="interVal" :timeVal="interValue" >
        <TimerDisplay :timer="count" />
        <ControlButton @isStarted="timerStarted" @isStopped="timerClosed" @isReset="timerReset" :disabled="disabled" />
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
        },
        
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
            disabled: false,
        }
    },
    methods: {
        increaseCount() {
            this.count++;
            // console.log(this.count);

        },
        interVal(val) {
            this.interValue = val;
        },
        timerStarted(val) {
            this.close = setInterval(this.increaseCount, 1000);
            this.disabled = val;
    
        },
        timerClosed() {
            this.disabled = true;
            clearInterval(this.close);
            // this.count = 0;
            this.disabled = false;
            // console.log(this.disabled);
            // console.log(this.disabled);
        },
        timerReset() {
            // console.log(this.count)
            this.count = 0;
        },
        
    }
}
</script>

<style>
    .timer-card{
        box-sizing: border-box;
        width: 200px;
        height: 90px;
        background-color: rgba(45, 52, 54, 0.5);
        border-radius: 5px;
        padding: 1%;
        margin-bottom: 10px;
        margin-right: 5px;
    }
</style>