<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
  if (isMenuOpen.value) {
    document.body.style.overflow = 'hidden';
  } else {
    document.body.style.overflow = '';
  }
};

const closeMenu = () => {
  isMenuOpen.value = false;
  document.body.style.overflow = '';
};
</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="/Layer_2.svg" alt="logo">
        <a href="#"><img src="/Vector.svg" alt="logo" class="logo-text"></a>
      </div>
      <nav class="navigation">
        <a href="#features">Features</a>
        <a href="#steps">How It Works</a>
        <a href="#price">Pricing</a>
        <button>Download Now</button>
      </nav>
      <div class="burger-btn" @click="toggleMenu" :class="{ active: isMenuOpen }">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <div class="mobile-menu" :class="{ open: isMenuOpen }" @click="closeMenu">
        <div class="menu-content " @click.stop>
          <nav>
            <a href="#features" @click="closeMenu">Features</a>
            <a href="#steps" @click="closeMenu">How It Works</a>
            <a href="#price" @click="closeMenu">Pricing</a>
            <button class="nav-btn mobile-btn">Download Now</button>
          </nav>
        </div>
      </div>

    </div>
  </header>
</template>

<style scoped>
header{
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  background: rgba(255, 255, 255, 0.8);
  width: 100%;
}
.container{
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  max-width: 1280px;
  margin: 0 auto;
  width: 100%;
  padding: 0 10px;
}
.navigation a{
  margin-right: 30px;
  font-size: 20px;
  font-weight: 500;
  cursor: pointer;
  color: black;
  text-decoration: none;
  position: relative;
  transition: color 0.3s ease;
}
/* Линия подчеркивания */
.navigation a::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 50%;
  width: 0;
  height: 2px;
  background: #A055FD;
  transition: all 0.3s ease;
  transform: translateX(-50%);
}
.navigation a:hover {
  color: #A055FD;
}
.navigation a:hover::after {
  width: 100%;
}
.navigation a:active{
  color: #3D71FF;
}
.navigation a:active::after{
  background: #3D71FF;
}
.navigation button{
  color: white;
  border: none;
  background: linear-gradient(to right, #A055FD, #E24A9A);
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s ease;
}
.navigation button:hover{
  transform: scale(1.1);
}
.navigation button:active{
  transform: scale(0.9);
}
.logo-text{
  margin-bottom: 9px;
  margin-left: 9px;
}
.burger-btn {
  display: none;
}
.mobile-menu {
  display: none;
}

@media (max-width: 768px) {
  .navigation {
    display: none;
  }
  .burger-btn {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 30px;
    height: 20px;
    cursor: pointer;
    z-index: 101; /* Поверх меню */
  }
  .burger-btn span {
    display: block;
    width: 100%;
    height: 3px;
    background-color: #333;
    transition: all 0.3s ease;
  }

  /* Анимация превращения в крестик */
  .burger-btn.active span:nth-child(1) {
    transform: rotate(45deg) translate(5px, 6px);
  }
  .burger-btn.active span:nth-child(2) {
    opacity: 0;
  }
  .burger-btn.active span:nth-child(3) {
    transform: rotate(-45deg) translate(5px, -6px);
  }

  .mobile-menu {
    display: flex;
    position: fixed;
    top: 0;
    right: 0;
    width: 100%;
    height: 100vh;
    z-index: 100;

    /* Скрыто по умолчанию */
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
    border-radius: 20px;
  }

  /* Класс open делает меню видимым */
  .mobile-menu.open {
    opacity: 1;
    visibility: visible;
  }

  .menu-content {
    width: 100%;
    height: 50%;
    background: rgba(255, 255, 255, 0.8);
    backdrop-filter: blur(15px);

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .mobile-menu nav {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }

  .mobile-menu a {
    font-size: 20px;
    font-weight: 500;
    cursor: pointer;
    color: black;
  }

  .mobile-btn {
    color: white;
    border: none;
    background: linear-gradient(to right, #A055FD, #E24A9A);
    padding: 10px;
    border-radius: 8px;
    font-size: 20px;
    font-weight: 500;
    cursor: pointer;
  }
}
</style>
