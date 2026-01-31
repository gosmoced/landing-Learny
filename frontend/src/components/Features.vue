<script setup>
import {ref} from "vue";

const features = ref([
  {
    title: "Choose Your Learning Buddy",
    text: "Pick from multiple AI avatar companions—each with unique personality and teaching style to match your preferences.",
    image: "/f1.svg"
  },
  {
    title: "Adaptive AI Learning",
    text: "Intelligent system that adapts topics, complexity, and teaching methods based on your level and progress.",
    image: "/f2.svg"
  },
  {
    title: "Voice-First Interaction",
    text: "Natural, conversational learning through voice. Engage in discussions, ask questions, and learn interactively.",
    image: "/f3.svg"
  },
  {
    title: "Dynamic Topic Selection",
    text: "Explore educational, creative, and entertainment content that evolves with your interests and goals.",
    image: "/f4.svg"
  },
  {
    title: "Comprehensive Progress Insights",
    text: "Track your learning journey with detailed analytics, achievements, and personalized recommendations.",
    image: "/f5.svg"
  },
  {
    title: "Guardian Dashboard",
    text: "Parents can monitor progress, control content access, and review detailed learning reports.",
    image: "/f6.svg"
  }
])
</script>

<template>
  <section class="features" id="features">

    <div class="container">
      <div class="features-headers">
        <h1>Intelligent Learning That Adapts to You</h1>
        <p>Advanced AI technology meets personalized education—choose your learning companion and explore any topic</p>
      </div>
      <div class="features-grid">
        <div class="features-card" v-for="(item, index) in features" :key="index">
          <div class="card-header">
            <img :src="item.image" :alt="item.title">
            <h3>{{ item.title }}</h3>
          </div>
          <p>{{ item.text }}</p>
        </div>
      </div>
    </div>

  </section>
</template>

<style scoped>
.features{
  margin-bottom: 150px;
}
.features-headers{
  text-align: center;
  max-width: 770px;
  margin: 0 auto;
}
.features-headers h1 {
  font-weight: 500;
  font-size: 40px;
  line-height: 70px;
}
.features-headers p {
  font-size: 20px;
  font-weight: 500;
  opacity: 50%;
  line-height: 30px;
}
.features-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  margin-top: 80px
}
.features-card{
  max-width: 370px;
  background: rgba(255, 255, 255, 0);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.5);
  border-top: 1px solid rgba(255, 255, 255, 0.8);
  border-left: 1px solid rgba(255, 255, 255, 0.8);
  box-shadow: 0 40px 80px rgba(0, 0, 0, 0.1);
  border-radius: 24px;
  padding: 15px;
}
.features-card h3 {
  display: inline-block;
  font-weight: 700;
  font-size: 18px;
  color: #384152;
  margin-left: 15px;
}
.features-card p {
  font-size: 16px;
  line-height: 24px;
  color: #384152;
  margin-top: 20px;
}
.card-header{
  display: flex;
  align-items: center;
}
@media (max-width: 1024px) {
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
    justify-items: center;
  }
}

@media (max-width: 768px) {
  .features-grid {
    grid-template-columns: 1fr;
  }
  .features-headers h1{
    line-height: 50px;
  }
}
@media (max-width: 500px) {
  .features-headers h1{
    font-size: 24px;
    line-height: 30px;
    padding: 10px;
  }
  .features-headers p{
    font-size: 16px;
    line-height: 24px;
    margin-bottom: -25px;
  }
}
</style>