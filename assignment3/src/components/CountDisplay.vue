<template>
    <div class="timer">
        <p>{{ timer }}</p>
    </div>
</template>

<script>
export default {
    name: "TimerDisplay",
    props: {
        timer: {
            type: Number,
            default: 0,
        },
    },
}
</script>

<style>
    .timer{
        display: flex;
        align-items: center;
        text-align: center;
        justify-content: center;
        box-sizing: border-box;
        width: 80%;
        height: 40%;
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 5px;
    }

    .timer p{
        font-family: sans-serif;
        text-align: center;
        color: #fff;
    }
</style>