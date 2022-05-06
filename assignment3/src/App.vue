<template>
  <div id="app">
    <div class="add-timer">
      <p @click="addCard">Click here to add Timer</p>
    </div>
    <!-- <div class="extra-button" @click="counter">Extra Button</div> -->
    <div class="holder">
      <div class="in-holder" v-for="(card, index) in cardList" :key="index">
      <TimerCard :timer="card.timer" />
      </div>
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
      content: {
        timer: 0,
      }
    }
  },
  methods: {
    addCard() {
      console.log("Button was clicked");
        this.cardList.push(this.content);
        console.log(this.cardList);
    },

    // counter() {
    //   console.log("Stared Counter");
    //   for(let card of this.cardList) {
    //     console.log(card.timer)
    //     setInterval(function() {
    //       console.log("Timer started")
    //       card.timer = card.timer + 1;
    //   }
    //   , 1000) 
    //   console.log(card);
    //   console.log(card.timer)
    //   }
    // }

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
  box-sizing: border-box;
  display: flex;
  width: 20%;
  height: 10%;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 1%;
  font-weight: 400;
  border-radius: 10px;
  font-size: 16px;
  margin-bottom: 20px;
  background-color: rgba(24, 44, 97, 0.4);
  color: #fff;
}

.add-timer p{
  cursor: pointer;
}

.holder{
  display: flex;
  flex-wrap: wrap;
  box-sizing: border-box;
  width: 100%;
  height: 570px;
  border-radius: 10px;
  padding: 2%;
  background-color: rgba(24, 44, 97, 0.4);
}
</style>
