<script setup>
import {ref} from "vue";
const steps = ref([
  {
    title: "Download & Set Up",
    text: "Download Learny and create your account. Customize your learning profile and preferences in minutes.",
    icon: "/steps1.svg",
    color: "pink"
  },
  {
    title: "Choose Your AI Companion",
    text: "Pick your perfect learning buddy from our AI avatars. Each one brings a unique approach to help you master any subject.",
    icon: "/steps2.svg",
    color: "blue"
  },
  {
    title: "Start Your Learning Journey",
    text: "Begin interactive sessions through voice or text. Watch your progress grow with personalized insights and achievements.",
    icon: "/steps3.svg",
    color: "yellow"
  }
])
</script>

<template>
  <section class="steps" id="steps">

    <div class="container">

      <div class="steps-wrapper">
        <div class="steps-card" v-for="(step, index) in steps" :key="index" :class="step.color">
          <div class="icon">
            <img :src="step.icon" :alt="step.title">
          </div>
          <h3>{{ step.title }}</h3>
          <p>{{ step.text }}</p>
        </div>
        <div class="line">
          <img src="/line1.svg" alt="line" class="line1">
          <img src="/line2.svg" alt="line" class="line2">
        </div>
      </div>

      <div class="steps-info">
        <h1>Get Started in <span><br>3 Simple Steps</span></h1>
      </div>

    </div>

  </section>
</template>

<style scoped>
.steps{
  margin-bottom: 150px;
}
.container{
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.steps-wrapper{
  position: relative;
  gap: 10px;
  display: flex;
  flex-direction: column;
}
.steps-card{
  max-width: 270px;
  width: 100%;
  background: rgba(255, 255, 255, 0);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.5);
  border-top: 1px solid rgba(255, 255, 255, 0.8);
  border-left: 1px solid rgba(255, 255, 255, 0.8);
  box-shadow: 0 40px 80px rgba(0, 0, 0, 0.1);
  border-radius: 24px;
  padding: 25px 15px;
  display: flex;
  align-items: center;
  flex-direction: column;
  z-index: 2;
}
.steps-card.blue{
  align-self: flex-end;
  margin-right: 35px;
}
.steps-card.pink, .steps-card.yellow {
  align-self: flex-start;
}
.icon{
  position: absolute;
  top: -50px
}
.steps-card h3{
  text-align: center;
  font-weight: 700;
  font-size: 20px;
  margin-top: 35px;
  margin-bottom: 10px;
}
.steps-card p{
  text-align: center;
  color: #384152;
}
.steps-info{
  display: flex;
  align-items: center;
  justify-content: center;
}
.steps-info h1 {
  font-size: 60px;
  font-weight: 400;
}
.steps-info h1 span {
  color: #8A4FFF;
  font-weight: bold;
  background: linear-gradient(to right, #A055FD, #E24A9A);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.line{
  position: absolute;
}
.line1{
  position: absolute;
  left: 215px;
  top: -40px;
  z-index: 1;
}
.line2{
  position: absolute;
  z-index: 1;
  left: 330px;
  top: 440px
}
@media(max-width: 1080px) and (min-width: 860px){
  .steps-wrapper{
    gap: 55px;
  }
  .line1{
    rotate: 35deg;
    top: 30px;
  }
  .line2{
    left: 280px;
    top: 460px;
  }
}
@media(max-width: 860px) and (min-width: 769px) {
  .steps-wrapper{
    gap: 55px;
  }
  .line1{
    rotate: 60deg;
    top: 50px;
  }
  .line2{
    left: 250px;
    top: 500px;
    rotate: -15deg;
  }
}
@media (max-width: 768px){
  .container {
    display: flex;
    flex-direction: column-reverse; }
  .steps-info{
    margin-bottom: 100px;
  }
}
@media (max-width: 550px) {
  .steps{
    margin-bottom: 100px;
  }
  .steps-info h1{
    font-size: 40px;
    text-align: center;
  }
  .steps-card {
    margin-bottom: 70px;
  }
  .steps-card.blue {
    margin-right: 0;
  }
  .line1{
    height: auto;
    width: 220px;
    left: 175px;
    rotate: 45deg;
    top: 40px;
  }
  .line2{
    left: 260px;
    top: 500px;
    rotate: -5deg;
  }
}
@media (max-width: 376px) {
  .line1{
    height: auto;
    width: 180px;
    left: 175px;
    rotate: 45deg;
    top: 90px;
  }
  .line2{
    height: auto;
    width: 90px;
    left: 250px;
    top: 500px;
    rotate: -20deg;
  }
}
@media (max-width: 350px) {
  .line1{
    height: auto;
    width: 120px;
    left: 175px;
    rotate: 45deg;
    top: 160px;
  }
  .line2{
    height: auto;
    width: 60px;
    left: 200px;
    top: 500px;
    rotate: -20deg;
  }
}
</style>