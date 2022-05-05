<template>
    <div class="control">
        <div class="start">
            <p @click="start">{{ str }}</p>
        </div>
        <div class="stop">
            <p @click="stop">{{ stp }}</p>
        </div>
    </div>
</template>

<script>


export default {
    name: "ControlButton",
    data () {
        return {
            str: "Start",
            stp: "Stop",
            count: "0",
        }
    },
    methods: {
        start() {
            this.emit("isClicked")
            setInterval(function(){
                
            }, 1000)
        },

        stop() {
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