<template>
  <div id="app">
    <div class="add-timer" @click:>
      <p> Click here to add Timer</p>
    </div>
    <div class="holder">
      <TimerCard />
    </div>
  </div>
</template>

<script>

import TimerCard from './components/TimerCard.vue'

export default {
  name: 'App',
  components: {
    TimerCard,
  },
  data() {
    return {
      cardList: [],
    }
  }
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
}

#app {
  box-sizing: border-box;
  width: 80%;
  height: 700px;
  margin: 1% auto;
  padding: 20px;
  border-radius: 10px;
  background-color: rgba(24, 44, 97, 0.8);
}

.add-timer{
  display: flex;
  box-sizing: border-box;
  width: 20%;
  height: 10%;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 1%;
  background-color: rgba(24, 44, 97, 0.4);
  color: #fff;
  font-weight: 400;
  border-radius: 10px;
  font-size: 16px;
  margin-bottom: 20px;
}

.holder{
  box-sizing: border-box;
  width: 100%;
  height: 570px;
  background-color: rgba(24, 44, 97, 0.4);
  border-radius: 10px;
  padding: 2%;
}
</style>
