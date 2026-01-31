<script setup>
import {ref} from "vue";
const designed = ref([
  {
    img: '/designed1.svg',
    title: 'English Language',
    text: 'Build vocabulary, grammar, speaking skills, and confidence through interactive conversations.',
  },
    {
    img: '/designed2.svg',
    title: 'Math & Logic',
    text: 'Practice arithmetic, problem-solving, and logical thinking in an easy, engaging way.',
  },
    {
    img: '/designed3.svg',
    title: 'Emotions & Well-Being',
    text: 'Learn to understand feelings, manage emotions, and stay confident and balanced.',
  },
    {
    img: '/designed4.svg',
    title: 'Soft Skills & Thinking',
    text: 'Improve focus, memory, creativity, critical thinking, and learning habits.',
  },
    {
    img: '/designed5.svg',
    title: 'Social Skills & Communication',
    text: 'Learn how to make friends, express thoughts clearly, resolve conflicts, and communicate respectfully.',
  },
    {
    img: '/designed6.svg',
    title: 'Science & The World',
    text: 'Discover how the world works — nature, space, technology, simple facts and “why” questions.',
  },
    {
    img: '/designed7.svg',
    title: 'Creativity & Imagination',
    text: 'Create stories, invent characters, explore ideas, and express yourself creatively.',
  },
    {
    img: '/designed8.svg',
    title: 'Life Skills',
    text: 'Build real-life habits: planning, responsibility, organization, time-management, self-care.',
  },
    {
    img: '/designed9.svg',
    title: 'Digital Safety',
    text: 'Understand internet safety, privacy, online behavior, and how to avoid scams and fake information.',
  },
    {
    img: '/designed10.svg',
    title: 'Hobbies & Interests',
    text: 'Conversations about games, sports, music, movies, animals, tech — everything kids love.',
  },
])
</script>

<template>
  <section class="designed">
    <div class="wrapper-designed">

      <div class="img-block">
        <img src="/bear.svg" alt="" class="img-bear">
        <img src="/iphone.svg" alt="">
        <img src="/samsung.svg" alt="" class="android">
      </div>

      <div class="text-block">
        <h1>Designed for Learners & Guardians</h1>
        <div class="card" v-for="(item, index) in designed" :key="index">
          <div class="card-wrapper">
            <img :src="item.img" alt="">
            <div>
              <h2>{{ item.title }}</h2>
              <p>{{ item.text }}</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
.designed{
  margin-bottom: 100px;
}
.wrapper-designed{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.img-block{
  width: 40%;
  position: relative;
}
.img-block img{
  display: block;
}
.img-block .img-bear{
  position: absolute;
  top: 60px;
  left: -50px;
}
.text-block{
  width: 60%;
  margin-top: 50px;
}
.text-block h1{
  font-size: 40px;
  font-weight: 500;
  margin-bottom: 30px;
}
.card-wrapper{
  display: flex;
  max-width: 575px;
}
.card-wrapper img{
  position: relative;
  top: -20px;
  margin-right: 10px;
}
.card-wrapper h2{
  font-size: 18px;
  font-weight: 700;
  margin-bottom: 5px;
}
.card-wrapper p{
  margin-bottom: 20px;
  line-height: 24px;
  color: #384152;
}
@media (max-width: 1350px){
  .img-block .img-bear{
    left: -5px;
  }
}
@media (max-width: 990px){
  .wrapper-designed{
    flex-direction: column;
  }
  .img-block {
    display: flex;
    width: 100%;
  }
  .img-block .img-bear{
    position: static;
    margin-right: -80px;
    margin-top: -220px;
    margin-left: 30px;
  }
  .img-block .android {
    margin-left: -50px;
  }
  .text-block{
    width: 100%;
  }
  .text-block h1{
    text-align: center;
  }
  .card{
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
@media (max-width: 910px){
  .img-block{
    margin-left: -75px;
  }
}
@media (max-width: 850px) {
  .img-block {
    justify-content: center;
    align-items: center;
    margin-left: 0;
  }
  .img-block .android{
    display: none;
  }
}
@media (max-width: 768px) {
  .text-block h1{
    text-align: start;
  }
  .card{
    justify-content: start;
    align-items: center;
  }
}
@media (max-width: 500px) {
  .img-block img{
    scale: 0.9;
  }
  .img-block .img-bear{
    margin-right: -130px;
  }
}
@media (max-width: 459px){
  .img-block{
    margin-bottom: -60px;
  }
  .img-block img {
    scale: 0.8;
    padding-left: 70px;
  }
  .img-block .img-bear{
    margin-right: -200px;
  }
  .card-wrapper img{
  top: -32px;
}
}
@media (max-width: 360px){
  .img-block img{
    scale: 0.7;
  }
  .img-block .img-bear{
    margin-right: -230px;
  }
}
@media (max-width: 353px){
  .card-wrapper img{
  top: -43px;
}
}
</style>