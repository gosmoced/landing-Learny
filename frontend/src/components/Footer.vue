<script setup>

</script>

<template>
  <footer class="footer">
    <div class="wrapper">

      <div class="top-footer">

        <div class="logo-footer">
          <div class="logo-block">
            <img src="/Layer_2.svg" alt="">
            <img src="/logo_text.svg" alt="" class="logo-text">
          </div>
          <p>Innovative AI-powered learning platform with adaptive education</p>
        </div>

        <div class="wrapper-navigation">
          <div class="navigation">
            <h2>Product</h2>
            <nav>
              <ul>
                <li><a href="">Features</a></li>
                <li><a href="">Pricing</a></li>
                <li><a href="">FAQ</a></li>
              </ul>
            </nav>
          </div>

          <div class="navigation">
            <h2>Company</h2>
            <nav>
              <ul>
                <li><a href="">About As</a></li>
                <li><a href="">Blog</a></li>
                <li><a href="">Contact</a></li>
              </ul>
            </nav>
          </div>

          <div class="navigation">
            <h2>Legal</h2>
            <nav>
              <ul>
                <li><a href="">Privacy Policy</a></li>
                <li><a href="">Terms of Service</a></li>
                <li><a href="">Safety</a></li>
              </ul>
            </nav>
          </div>
        </div>
      </div>

      <div class="bottom-footer">
        <div class="line"></div>
        <p>© 2025 Learny. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer{
  background-color: #101828;
  color: white;
}
.wrapper{
  max-width: 1280px;
  width: 95%;
  margin: 0 auto;
  padding: 50px 0;
}
.top-footer{
  padding-bottom: 50px;
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 20px;
}
.wrapper-navigation{
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
.logo-footer{
  max-width: 270px;
  width: 100%;
  p{
    margin-top: 25px;
    font-size: 14px;
    line-height: 24px;
  }
  .logo-text{
    position: relative;
    left: 12px;
    top: -8px;
  }
}
.navigation{
  max-width: 300px;
  width: 100%;
  h2{
    font-weight: 600;
    font-size: 20px;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  ul{
    list-style: none;
    li{
      font-size: 14px;
      font-weight: 400;
      margin-top: 15px;
    }
    a{
      color: white;
    }
  }
}
.bottom-footer{
  .line{
    width: 100%;
    height: 1px;
    background: #ECE5FA;
    opacity: 10%;
  }
  p{
    text-align: center;
    font-weight: 400;
    font-size: 14px;
    margin-top: 40px;
  }
}
@media(max-width: 693px){
  .logo-footer{
    p{
      margin-top: 10px;
    }
  }
}
@media(max-width: 555px){
  .top-footer{
    grid-template-columns: 1fr;
  }
}
@media (max-width: 440px){
  .top-footer{
    .logo-footer{
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      .logo-block{
        margin-left: -10px;
      }
      p{
        text-align: center;
      }
    }
  }
  .top-footer > .logo-footer{justify-self: center;}
  .wrapper-navigation{
    flex-direction: column;
    .navigation{
      width: 100%;
      max-width: none;
      margin-left: 10px;
      h2{
        font-size: 30px;
      }
      a{
        font-size: 20px;
      }
    }
  }
}
</style>