<script setup>

</script>

<template>
  <section class="ready">
    <div class="container full-width">
      <div class="content">
        <div class="headers-ready">
          <h1>Ready to Transform Your Learning Experience?</h1>
          <p>Join thousands of learners discovering smarter ways to learn with AI</p>
        </div>
        <div class="img-block">
          <a href="#" aria-label="button Google Play"><img src="/googleplay2.svg" alt="Google Play"></a>
          <a href="#" aria-label="button App Store"><img src="/appstore2.svg" alt="App Store"></a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.ready{
  margin-top: -180px;
}
.container {
  min-height: 430px;
  background: linear-gradient(to right, #A055FD, #E24A9A);
  clip-path: polygon(0 40%, 100% 0%, 100% 100%, 0 100%);
  overflow: hidden;
}
.full-width{
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
}
.content{
  max-width: 1280px;
  width: 95%;
  margin: 0 auto;
  padding-top: 150px;
  padding-left: 35px;
  padding-right: 35px;
}
@media(max-width: 768px){
  .content{
    width: 95%;
    margin: 0 auto;
  }
}
.headers-ready{
  text-align: center;
  margin: 30px 0;
  color: white;
}
.headers-ready h1{
  font-weight: 500;
  font-size: 40px;
  margin-bottom: 20px;
}
.headers-ready p{
  opacity: 50%;
  font-size: 20px;
  font-weight: 500;
}
.img-block{
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 30px;
  padding-bottom: 50px;
}
.img-block a {
  display: inline-block;
  transition: all 0.3s ease;
}
/* Эффект при наведении */
.img-block a:hover {
  transform: translateY(-5px);
  filter: drop-shadow(0 10px 15px rgba(0, 0, 0, 0.2));
}
/* Эффект при нажатии (клик) */
.img-block a:active {
  transform: translateY(-2px);
  filter: drop-shadow(0 5px 10px rgba(0, 0, 0, 0.15));
}
@media (max-width: 619px){
  .ready{
    margin-top: 0;
  }
  .container {
  clip-path: polygon(0 30%, 100% 0%, 100% 100%, 0 100%);
 }
}
@media (max-width: 500px){
  .headers-ready{
    margin-top: 0;
  }
  .headers-ready h1{
  font-size: 24px;
  line-height: 30px;
  }
  .headers-ready p{
    font-size: 16px;
    line-height: 24px;
  }
}
@media (max-width: 450px){
  .img-block{
    flex-direction: column;
    gap: 20px;
  }
}
@media (max-width: 400px){
  .container {
    clip-path: polygon(0 25%, 100% 0%, 100% 100%, 0 100%);
  }
}
</style>