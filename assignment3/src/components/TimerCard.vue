<template>
    <div class="timer-card">
        <TimerDisplay />
        <ControlButton />
    </div>
</template>

<script>

import TimerDisplay from "./CountDisplay.vue"
import ControlButton from "./Control.vue"

export default {
    name: "TimerCard",
    components: {
        TimerDisplay,
        ControlButton,
    },
    data() {
        return {
            name: "0",
        }
    }
}
</script>

<style>
    .timer-card{
        display: none;
        box-sizing: border-box;
        width: 200px;
        height: 100px;
        background-color: rgba(248, 239, 186, 0.8);
        border-radius: 5px;
        padding: 1%;
    }
</style>