<script setup>
import {ref} from "vue";
const companion = ref([
       {
      name: "Emma",
      title: "Friendly & Patient",
      text: "Your enthusiastic learning companion who makes every topic exciting. Emma specializes in breaking down complex concepts into simple, digestible pieces.",
      image: "/name1.svg",
      skill1: "Great for beginners",
      skill2: "Conversational style",
      image_skill1: '/mingcute_ai-fill.svg',
      image_skill2: '/mynaui_chat-solid.svg'
  },
    {
      name: "Mia",
      title: "Creative & Inspiring",
      text: "Your creative mentor who brings imagination to learning. Mia excels at arts, languages, and creative thinking exercises.",
      image: "/name2.svg",
      skill1: "STEM expertise",
      skill2: "Advanced learners",
      image_skill1: 'fluent_brain-sparkle-20-filled.svg',
      image_skill2: 'mingcute_flash-fill.svg'
  },
    {
      name: "More Companions",
      title: "Coming Soon",
      text: "A diverse range of new Al learning companions with unique specializations, teaching styles, and expertise are on the\n" +
          "way to join your journey.",
      image: "/name3.svg",
      skill1: "New Personalities",
      skill2: "Specialized Subjects",
      image_skill1: '/fluent_people-20-filled.svg',
      image_skill2: 'mdi_color.svg'
  },
    ]
)
</script>

<template>
  <section class="companion">
    <div class="container">
      <div class="companion-headers">
        <h1>Choose Your Perfect Learning Companion</h1>
        <p>Each AI avatar has a unique personality, teaching style, and expertise. Find the one that resonates with you and makes learning feel natural and fun.</p>
      </div>
      <div class="companion-card">
        <div class="card" v-for="(item, index) in companion" :key="index">
          <img class="main-image" :src="item.image" alt="">
          <h2>{{ item.name }}</h2>
          <p :class="`title-${index}`">{{ item.title }}</p>
          <p class="text">{{ item.text }}</p>
          <div class="skill">
            <div class="skill1">
              <img :src="item.image_skill1" alt="">
              <span :class="`skill-text-${index}`">{{ item.skill1 }}</span>
            </div>
            <div class="skill2">
              <img :src="item.image_skill2" alt="">
              <span :class="`skill-text-${index}`">{{ item.skill2 }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.companion-headers{
  text-align: center;
  margin: 0 auto;
  width: 100%;
  max-width: 850px;
  margin-bottom: 100px;
}
.companion-headers h1 {
  font-weight: 500;
  font-size: 40px;
  margin-bottom: 10px;
}
.companion-headers p {
  font-size: 20px;
  font-weight: 500;
  opacity: 50%;
  line-height: 30px;
}
.companion-card{
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 5px;
}
.card{
  min-height: 346px;
  width: 370px;
  height: auto;
  max-width: 100%;
  padding: 0 10px;
  background: rgba(255, 255, 255, 0);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.5);
  border-top: 1px solid rgba(255, 255, 255, 0.8);
  border-left: 1px solid rgba(255, 255, 255, 0.8);
  box-shadow: 0 40px 80px rgba(0, 0, 0, 0.1);
  border-radius: 24px;
  text-align: center;
  margin-bottom: 70px;
  z-index: 2;
}
.main-image{
  position: relative;
  top: -40px;
}
.card h2{
  margin-bottom: 10px;
}
.title-0 {
  background-color: #e4cee3;
  color: #d35090;
  border-radius: 10px;
  padding: 3px 3px;
  width: 150px;
  margin: 0 auto;
  font-weight: 500;
  margin-bottom: 20px;
}
.title-1 {
  background-color: #ced6f9;
  color: #4b7cf8;
  border-radius: 10px;
  padding: 3px 3px;
  width: 165px;
  margin: 0 auto;
  font-weight: 500;
  margin-bottom: 20px;
}
.title-2 {
  background-color: #dec5f2;
  color: #a55be5;
  border-radius: 10px;
  padding: 3px 3px;
  width: 165px;
  margin: 0 auto;
  font-weight: 500;
  margin-bottom: 20px;
}
.text{
  color: #384152;
  line-height: 24px;
}
.skill {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
  margin-top: 20px;
}
.skill1 span, .skill2 span{
  position: relative;
  top: -5px;
  font-weight: 400;
  font-size: 14px;
  margin-left: 2px;
}
.skill-text-0{
  color: #d35090;
}
.skill-text-1{
  color: #4b7cf8;
}
.skill-text-2{
  color: #a55be5;
}
@media (max-width: 800px){
  .companion-card{
    flex-direction: column;
    align-items: center;
  }
}
@media (max-width: 500px) {
  .companion-headers h1{
    font-size: 24px;
    line-height: 30px;
    padding: 10px;
  }
  .companion-headers p{
    font-size: 16px;
    line-height: 24px;
  }
}
</style>