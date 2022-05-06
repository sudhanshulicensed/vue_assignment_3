<template>
    <div class="control">
        <div class="start">
            <p @click="start">Start</p>
        </div>
        <div class="stop">
            <p @click="stop">Reset</p>
        </div>
    </div>
</template>

<script>


export default {
    name: "ControlButton",
    methods: {
        start() {
            this.$emit("isStarted")
        },

        stop() {
            this.$emit("isStopped")
        }
    }
}
</script>

<style>
    .control{
        display: flex;
        justify-content: space-evenly;
        width: 90%;
        height: 60%;
        margin-left: auto;
        margin-right: auto;
    }

    .start, .stop{
        box-sizing: border-box;
        width: 60px;
        padding-top: 20px;
        border: 1px solid black;
    }

    .start p, .stop p{
        text-align: center;
    }
</style>