<script setup>

</script>

<template>
  <section class="price" id="price">

    <div class="price-headers">
      <h1>Start Free, Upgrade Anytime</h1>
      <p>Try Learny for free or unlock unlimited learning with Premium</p>
    </div>

    <div class="wrapper-price">

      <div class="wrapper-left-block">
        <div class="left-block">
          <h2>Free</h2>
          <p><span>0$ </span>forever</p>
          <p>Perfect to explore AI learning</p>
          <button>Get Started Free</button>
          <ul>
            <li><img src="/Close.svg" alt=""><span>Unlimited Questions</span></li>
            <li class="privileges"><img src="/Check.svg" alt=""><span>Guardian controls</span></li>
            <li><img src="/Check.svg" alt=""><span>Access to AI learning buddies</span></li>
            <li class="privileges"><img src="/Check.svg" alt=""><span>Avatar selection</span></li>
            <li><img src="/Check.svg" alt=""><span>Basic progress reports</span></li>
          </ul>
        </div>
      </div>

      <div class="wrapper-right-block">
        <div class="most-popular">
          <img src="/small_crown.svg" alt=""><span>Most Popular</span>
        </div>
        <img src="/crown.png" alt="" class="crown">
        <div class="right-block">
          <h2>Premium</h2>
          <p><span>9.99$ </span>/month</p>
          <p>Unlimited learning potential</p>
          <button>Upgrade to Premium</button>
          <ul>
            <li><img src="/Check.svg" alt=""><span>Unlimited Questions</span></li>
            <li class="privileges"><img src="/Check.svg" alt=""><span>Advanced analytics</span></li>
            <li><img src="/Check.svg" alt=""><span>Access to AI learning buddies</span></li>
            <li class="privileges"><img src="/Check.svg" alt=""><span>Deep Learning</span></li>
            <li><img src="/Check.svg" alt=""><span>Extended progress reports</span></li>
            <li class="privileges"><img src="/Check.svg" alt=""><span>Adaptive Content</span></li>
            <li><img src="/Check.svg" alt=""><span>Guardian controls</span></li>
            <li class="privileges"><img src="/Check.svg" alt=""><span>Avatar selection</span></li>
          </ul>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
.price-headers p, .price h1{
  text-align: center;
}
.price-headers h1{
  font-weight: 500;
  font-size: 40px;
  margin-bottom: 10px;
}
.price-headers p{
  opacity: 50%;
  font-weight: 500;
  font-size: 20px;
  margin-bottom: 50px;
}
.wrapper-price{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.wrapper-left-block, .wrapper-right-block{
  max-width: 572px;
  width: 100%;
  min-height: 435px;
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 50px;
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.5);
  border-top: 1px solid rgba(255, 255, 255, 0.8);
  border-left: 1px solid rgba(255, 255, 255, 0.8);
  box-shadow: 0 40px 80px rgba(0, 0, 0, 0.1);
  border-radius: 24px;
  margin-bottom: 150px;
}
.wrapper-price h2{
  font-size: 32px;
  font-weight: 500;
}
.left-block p:first-of-type span,
.right-block p:first-of-type span{
  font-size: 40px;
  font-weight: 600;
}
.left-block p:first-of-type,
.right-block p:first-of-type{
  font-size: 20px;
  font-weight: 300;
}
.left-block p:last-of-type,
.right-block p:last-of-type{
  font-size: 16px;
  font-weight: 500;
  margin-top: 5px;
  margin-bottom: 15px;
}
.left-block button, .right-block button{
  width: 100%;
  height: 60px;
  padding: 0;
  border-radius: 16px;
  border: none;
  font-weight: 500;
  font-size: 16px;
  margin-bottom: 15px;
  cursor: pointer;
  transition: all 0.3s ease;
}
.left-block button{
  background: transparent;
  backdrop-filter: none;
  -webkit-backdrop-filter: none;
  border: 1px solid rgba(0, 0, 0, 0.2);
}
.right-block button{
  background: linear-gradient(to right, #A055FD, #E24A9A);
  color: white;
}
.left-block button:hover, .right-block button:hover{
  transform: translateY(-5px);
}
.left-block button:active, .right-block button:active{
  transform: translateY(-2px);
}
.wrapper-price ul{
  list-style: none;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.wrapper-price ul li{
  padding-bottom: 10px;
}
.wrapper-price ul li span{
  position: relative;
  top: -11px;
  left: 10px;
  color: #384152;
  line-height: 25px;
}
.wrapper-price .privileges{
  margin-left: 45px;
}
/* Код для создания градиентной рамки */
.wrapper-right-block {
  position: relative;
  border-color: transparent;
  z-index: 10;
}
/* 2. Создаем градиентную рамку через псевдоэлемент */
.wrapper-right-block::before {
  content: "";
  position: absolute;
  inset: -1px;
  border-radius: 24px;
  padding: 2px; /* Толщина рамки */
  background: linear-gradient(to right, #A055FD, #E24A9A);
  -webkit-mask:
     linear-gradient(#fff 0 0) content-box,
     linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  pointer-events: none;
}
.most-popular{
  position: absolute;
  background: linear-gradient(to right, #A055FD, #E24A9A);
  color: white;
  top: -20px;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 10px;
  padding: 5px 20px;
  white-space: nowrap;
}
.most-popular span{
  position: relative;
  top: -5px;
  left: 5px;
}
.crown{
  position: absolute;
  height: 70%;
  left: 350px;
  top: -190px;
  rotate: 25deg;
}
@media (max-width: 1230px){
  .wrapper-price{
    flex-direction: column;
  }
}
@media (max-width: 619px){
  .wrapper-price ul{
    grid-template-columns: 1fr;
  }
  .wrapper-price .privileges{
  margin: 0
  }
  .crown{
    display: none;
  }
  .wrapper-left-block, .wrapper-right-block{
    margin-bottom: 50px;
  }
}
@media (max-width: 500px){
  .price-headers h1{
  font-size: 24px;
}
.price-headers p{
  font-size: 16px;
  line-height: 24px;
}
}
</style>