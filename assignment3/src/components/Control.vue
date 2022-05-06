<template>
    <div class="control">
        <button @click="start" class="start" :disabled="disabled" >
            Start
        </button>
        <button @click="stop" class="stop">
            Stop
        </button>
        <button @click="reset" class="reset">
            Reset
        </button>
    </div>
</template>

<script>

export default {
    name: "ControlButton",
    props: {
        disabled: {
            type: Boolean,
            default: false,
        }
    },
    methods: {
        start() {
            this.$emit("isStarted", true)
        },

        stop() {
            this.$emit("isStopped")
        },

        reset() {
            this.$emit("isReset")
        }
    }
}
</script>

<style>
    .control{
        display: flex;
        justify-content: space-evenly;
        width: 90%;
        height: 40%;
        margin-left: auto;
        margin-right: auto;
    }

    .start, .stop, .reset{
        display: flex;
        align-items: center;
        text-align: center;
        justify-content: center;
        box-sizing: border-box;
        width: 60px;
        border-radius: 5px;
        border: 1px solid black;
        cursor: pointer;
    }

    .start p, .stop p{
        text-align: center;
    }
</style>