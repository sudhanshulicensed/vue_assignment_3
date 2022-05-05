<template>
    <div class="timer">
        <p>{{ timer }}</p>
    </div>
</template>

<script>
export default {
    name: "TimerDisplay",
    data() {
        return {
            timer: "0",
        }
    }
}
</script>

<style>
    .timer{
        box-sizing: border-box;
        width: 80%;
        height: 30%;
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 5px;
    }

    .timer p{
        text-align: center;
    }
</style>