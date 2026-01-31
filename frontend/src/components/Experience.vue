<script setup>
import {ref} from "vue";
const experience = ref([
  {
    img: '/time.svg',
    title: 'Switch Between Avatars',
    text: 'Change your learning buddy anytime to match your current subject or mood'
  },
    {
    img: '/time.svg',
    title: 'Unique Teaching Styles',
    text: 'Each avatar adapts their approach based on your learning preferences and progress'
  },
    {
    img: '/time.svg',
    title: 'Build a Connection',
    text: 'Your chosen avatar remembers your progress and adjusts to your evolving needs'
  },
])
</script>

<template>
  <section class="experience">
    <div class="container full-width">
      <div class="content">
        <div class="content-wrapper">

          <div class="text-block">
          <h1>Personalize Your Experience</h1>
          <div class="wrapper-card">
            <div class="card" v-for="(item, index) in experience" :key="index">
              <img :src="item.img" alt="">
              <div>
                <h2>{{ item.title }}</h2>
                <p>{{ item.text }}</p>
              </div>
            </div>
          </div>
          </div>

        <div class="img-block">
          <img src="/weeklyActivity.svg" alt="" class="weeklyActivity">
          <img src="/dailyChatter.svg" alt="" class="dailyChatter">
          <img src="/getConsistent.svg" alt="" class="getConsistent">
          <img src="/topExplorer.svg" alt="" class="topExplorer">
          <img src="/avatar.svg" alt="" class="avatar">
          <img src="/voice.svg" alt="" class="voice">
          <img src="/overview.svg" alt="" class="overview">
          <img src="/reports.svg" alt="" class="reports">
          <img src="/star.svg" alt="" class="star">
          <img src="/star.svg" alt="" class="star2">
          <img src="/star.svg" alt="" class="star3">
          <img src="/star.svg" alt="" class="star4">
        </div>

        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.experience{
  margin-top: -100px;
}
.container{
  min-height: 666px;
  background: linear-gradient(to right, #3D71FF, #9C4BFF);
  clip-path: polygon(0 0, 100% 20%, 100% 100%, 0 80%);
  overflow: hidden;
  /* Включает аппаратное ускорение */
  transform: translate3d(0, 0, 0);
  will-change: transform;
}
.content{
  max-width: 1280px;
  width: 95%;
  margin: 0 auto;
  padding: 0 10px;
  padding-top: 150px;
}
@media(max-width: 768px){
  .content{
    width: 95%;
    margin: 0 auto;
  }
}
.content-wrapper{
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
}
.full-width{
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
}
h1{
  font-weight: 500;
  font-size: 40px;
  margin-bottom: 30px;
}
.card{
  display: flex;
  gap: 10px;
  max-width: 595px;
  width: 100%;
  margin-bottom: 30px;
}
.card img{
  margin-top: -17px;
}
.card h2{
  font-weight: 700;
  font-size: 18px;
  margin-bottom: 5px;
}
.card p{
  line-height: 24px;
}
.img-block{
  position: relative;
  max-width: 500px;
  width: 100%;
  /* Изолируем слой с картинками, чтобы они не перерисовывали фон */
  transform: translate3d(0, 0, 0);
  pointer-events: none;
}
.img-block img{
  position: absolute;
}
.img-block .weeklyActivity {
  top: -260px;
  left: 150px;
}
.img-block .dailyChatter {
  top: -100px;
  left: -50px;
}
.img-block .getConsistent {
  left: 170px;
  top: 40px;
}
.img-block .topExplorer {
  top: 150px;
  left: 20px;
  z-index: 3;
}
.img-block .voice{
  top: 150px;
  left: 320px;
  z-index: 2;
}
.img-block .overview{
  top: 130px;
  left: 400px;
}
.img-block .reports{
  top: -180px;
  left: 80px;
}
.img-block .avatar{
  left: 40px;
  top: 20px;
}
.img-block .star{
  top: 90px
}
.img-block .star2{
  top: -170px;
  left: 490px;
}
.img-block .star3{
  top: -170px;
  width: 25px;
  rotate: -30deg;
}
.img-block .star4{
  left: 500px;
  top: 130px;
  width: 50px;
}
@media(max-width: 1070px){
  .container{
    min-height: 800px;
  }
}
@media(max-width: 900px) {
  .content-wrapper {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .container {
    min-height: 1250px;
  }
  .content {
    padding-top: 200px;
  }
  .img-block {
    top: 200px;
  }
}
@media(max-width: 660px){
  .container{
    clip-path: polygon(0 0, 100% 10%, 100% 100%, 0 90%);
    min-height: 1050px;
  }
  .content{
    padding-top: 100px;
  }
}
@media(max-width: 596px){
  .container{
    min-height: 1100px;
  }
}
@media(max-width: 570px) and (min-height: 450px){
  .container{
    min-height: 1100px;
  }
  .img-block img{
    transform: scale(0.9);
  }
  .img-block .weeklyActivity, .img-block .getConsistent{
    left: +15%;
  }
  .img-block .voice{
    left: +55%;
  }
  .img-block .overview{
    left: +65%;
  }
  .img-block .reports{
    left: +5%;
  }
  .img-block .avatar{
    left: -5%;
  }
  .img-block .topExplorer{
    left: -5%;
  }
  .img-block .star{
    top: -15%;
  }
  .img-block .star2, .img-block .star4{
    left: 25%;
  }
}
@media(max-width: 450px){
  .card p{
    font-size: 14px;
    line-height: 20px
  }
  .container{
    min-height: 1200px;
  }
  .content{
    padding-top: 100px;
  }
  .img-block .weeklyActivity {
    top: -250px;
    left: -20px;
  }
  .img-block .dailyChatter {
    top: 10px;
    left: -30px;
    rotate: -20deg;
  }
  .img-block .getConsistent {
    left: 80px;
    top: 270px;
    rotate: 20deg;
  }
  .img-block .topExplorer {
    top: 150px;
    left: -20px;
  }
  .img-block .voice{
    top: 70px;
    left: 180px;
  }
  .img-block .overview{
    top: 220px;
    left: 270px;
  }
  .img-block .reports{
    top: -220px;
    left: 280px;
  }
  .img-block .avatar{
    left: -10px;
    top: 240px;
  }
  .img-block .star{
    top: 130px;
    left: 70px;
  }
  .img-block .star2{
    top: -170px;
    left: 200px;
  }
  .img-block .star3{
    top: -170px;
    width: 25px;
    rotate: -30deg;
  }
  .img-block .star4{
    left: 230px;
    top: 230px;
    width: 50px;
  }
  .img-block img{
    transform: scale(0.9);
  }
}
@media(max-width: 380px){
  .container{
    min-height: 1220px;
  }
  .img-block{
    margin-left: -70px;
  }
  .img-block img{
    transform: scale(0.7);
  }
}
@media(max-width: 351px){
  .container{
    min-height: 1300px;
  }
}
</style>