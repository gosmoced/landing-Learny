<script setup>

</script>

<template>
  <section class="hero">

      <div class="hero-content">
        <h1>Your Personal <br> <span>AI Learning Companion</span></h1>
        <p class="subtitle">
          Choose your perfect learning buddy from our AI avatars. Adaptive, personalized education that evolves with you—whether you're a curious learner or seeking mastery in any subject.
        </p>
        <div class="store-buttons">
          <a href="#" aria-label="button Google Play">
            <img class="sb-1" src="/googleplay.svg" alt="Google Play">
          </a>
          <a href="#" aria-label="button App Store">
            <img class="sb-2" src="/appstore.svg" alt="App Store">
          </a>
        </div>
        <div class="rating-container">
          <div class="rating">
            <img src="/Group%20319.svg" alt="Star">
            <p>4.9 out of 5 stars</p>
          </div>
          <div class="line"></div>
          <div class="rating-count">
            <h2>50K+</h2>
            <p>Active Learners</p>
          </div>
        </div>
      </div>

      <div class="hero-image">
        <div class="message m-color ms-1">Hi! Are you here to learn with me today?</div>
        <div class="message m-white ms-2">Hi! Yes, I’m here and ready. What would you like to learn?</div>
        <div class="message m-color ms-3">Can we do something fun?</div>
        <div class="message m-white ms-4">Of course! I can show you a cool mini-lesson. Do you want math,<br>animals, or a surprise?</div>
        <div class="message m-color ms-5">A surprise! 😀</div>
      </div>

  </section>
</template>

<style scoped>
.hero {
  padding-top: 100px;
  padding-bottom: 200px;
  display: flex;
  align-items: center;
  gap: 100px;
  justify-content: space-between;

}
.hero-image{
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 20px;
  width: 100%;
  max-width: 450px;
  padding: 20px;
}
h1 {
  font-size: 60px;
  line-height: 70px;
  font-weight: 400;
  margin-bottom: 10px;
}
h1 span {
  color: #8A4FFF;
  font-weight: bold;
  background: linear-gradient(to right, #A055FD, #E24A9A);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  display: inline-block;
}
.subtitle {
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 30px;
  line-height: 37px;
  width: 100%;
  max-width: 690px;
}
.store-buttons {
  display: flex;
  gap: 20px;
  margin-bottom: 40px;
}

.store-buttons a {
  display: inline-block;
  transition: all 0.3s ease;
}
/* Эффект при наведении */
.store-buttons a:hover {
  transform: translateY(-5px);
  filter: drop-shadow(0 10px 15px rgba(0, 0, 0, 0.2));
}
/* Эффект при нажатии (клик) */
.store-buttons a:active {
  transform: translateY(-2px);
  filter: drop-shadow(0 5px 10px rgba(0, 0, 0, 0.15));
}

.rating-container{
  display: flex;
  gap: 20px;
  align-items: center;
}
.rating-container p {
  font-size: 16px;
  font-weight: 500;
  line-height: 30px;
}
h2 {
  font-weight: 700;
  font-size: 33px;
}
.line {
  height: 60px;
  width: 3px;
  background: black;
  opacity: 20%;
}
.message{
  padding: 15px 10px;
  font-size: 16px;
  display: inline-block;
  line-height: 22px;
  max-width: 85%;
  width: fit-content;
  position: relative;
  cursor: default;
  overflow: hidden;
}
.m-color{
  color: white;
  background: linear-gradient(to right, #A055FD, #E24A9A);
  border-radius: 20px 20px 4px 20px;
  align-self: flex-end;
}
.m-white{
  background: aliceblue;
  border-radius: 4px 20px 20px 20px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  z-index: 2;
  width: 272px;
  align-self: flex-start;
}
.ms-1{
  transform: rotate(-6deg);
  width: 205px;
}
.ms-2{
  transform: rotate(6deg);
  margin-top: -25px;
}
.ms-3{
  transform: rotate(6deg);
  width: 150px;
  margin-top: -20px;
  margin-right: 10px;
}
.ms-4{
  transform: rotate(-6deg);
  margin-top: -25px;
}
.ms-5{
  transform: rotate(6deg);
  margin-top: -35px;
  width: 130px;
  margin-right: 25px;
}

/* Эффект блика */
.message::after {
  content: '';
  position: absolute;
  top: 0;
  left: -150%;
  width: 80%;
  height: 100%;
  /* Градиент: прозрачный -> белый полупрозрачный -> прозрачный */
  background: linear-gradient(
    to right,
    rgba(255, 255, 255, 0) 0%,
    rgba(255, 255, 255, 0.4) 50%,
    rgba(255, 255, 255, 0) 100%
  );
  transform: skewX(-25deg); /* Наклон полоски */
  pointer-events: none;     /* Чтобы блик не перекрывал текст для выделения */
  z-index: 10;
}
/* 3. Запускаем анимацию при наведении */
.message:hover::after {
  animation: messageShine 1s;
}
/* 4. Сама анимация движения */
@keyframes messageShine {
  0% {
    left: -100%;
  }
  100% {
    left: 200%;
  }
}
.message.m-white::after {
  /* Чуть более заметный блик для белого фона (слегка сероватый) */
  background: linear-gradient(
    to right,
    rgba(255, 255, 255, 0) 0%,
    rgba(220, 220, 220, 0.5) 50%,
    rgba(255, 255, 255, 0) 100%
  );
}

@media(max-width: 860px){
  .hero-image{
    padding-left: 0;
  }
}
@media(max-width: 840px){
  .hero-image{
    margin-left: -60px;
  }
}
@media (max-width: 768px){
  .hero {
    flex-direction: column-reverse;
    align-items: center;
    gap: 40px;
    padding-bottom: 100px;
  }
  .hero-image{
    margin-left: 0;
  }
}
@media (max-width: 426px) {
  .hero {
    flex-direction: column-reverse;
    align-items: center;
    text-align: start;
    gap: 40px;
    padding-bottom: 100px;
  }
  .hero-content {
    width: 100%;
    max-width: 100%;
    box-sizing: border-box;
  }
  .hero-image{
    padding: 0;
  }
  h1 {
    font-size: 50px;
    line-height: 50px;
  }
  .subtitle{
    font-size: 16px;
    line-height: 24px;
  }
  .store-buttons {
    justify-content: center;
  }
  .store-buttons img{
    height: auto;
    width: 170px;
  }
  .rating img {
    height: auto;
    width: 152px;
  }
  .rating-count h2{
    font-size: 32px;
  }
}
@media (max-width: 375px) {
  .store-buttons img{
    height: auto;
    width: 145px;
  }
  .rating-count p {
    line-height: 15px;
  }
}
</style>