<template>
  <div id="nav">
      <div class="logoBox">
        <a href="#"><img class="logo" src="@/assets/logo.png" alt="logo"></a>
      </div>
      <div>
        <input type="checkbox" id="click">
      <label for="click" class="menu-btn">
        <i class="fas fa-bars"></i>
      </label>
      <ul class="menu">
        <li><a href="#">Propiedades<i class="fa fa-chevron-down"></i></a></li>
        <li><a href="#">Compradores<i class="fa fa-chevron-down"></i></a></li>
        <li><a href="#">Vendedores<i class="fa fa-chevron-down"></i></a></li>
        <li><a href="#">Sobre nosotros<i class="fa fa-chevron-down"></i></a></li>
        <li><a href="#">Blog<i class="fa fa-chevron-down"></i></a></li>
        <li><a href="#contact" class="contact">Contacto<i class="fa fa-chevron-down"></i></a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style lang="scss">
#nav {
  display: flex;
  height: 80px;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  z-index: 3;
  position:absolute;
  top: 0px;
  padding: 20px 0;
  background: linear-gradient(to bottom,rgba(0,0,0,0.65) 0%,rgba(0,0,0,0) 100%);

  .logo {
    width: 140px;
    height: 30px;
    margin-left: 5em;
  }
  .logo:hover{
    color:#dfebf5;
  }

  .menu{
    margin-right: 100px;
  }
}

#nav ul{
    display: flex;
    flex-wrap: wrap;
    list-style: none;
  }
  #nav ul li{
    margin: 0 2px;
  }
  #nav ul li a{
    color: #fff;
    font-size: 16px;
    padding: 12px 12px;
    font-weight: 400;
    text-decoration: none;
    cursor: pointer;
    display: inline-block;
    position: relative;
    border-width: 0 0 0 1px;
    text-transform: uppercase;
    line-height: 1;
  }

  i {
      font-size: 9px;
      margin-left: 3px;
      margin-top: -3px;
      vertical-align: middle;
  }

  #nav ul li .contact {
    font-weight: bold;
    font-size: 0.88rem;
    padding: 10px 20px;
    border-radius: 5px;
    background: #a5d7d5;
  }

  #nav ul li .contact:hover {
    background: #a2efdf;
  }

  #nav .menu-btn i{
    color: #fff;
    font-size: 22px;
    padding: 0 30px;
    cursor: pointer;
    display: none;
  }

  input[type="checkbox"] {
    display: none;
  }
  @media (max-width: 1000px){
    #nav{
      height: 55px;
      padding: 0 40px 0 50px;
      justify-content: space-between;
    }
  }
  @media (max-width: 1000px) {
    #nav .menu-btn i{
      display: block;
    }
    #click:checked ~ .menu-btn i:before{
      content: "\f00d";
    }
    #nav ul{
      position: fixed;
      top: 55px;
      left: -100%;
      background: #222121;
      height: 100vh;
      width: 100%;
      text-align: center;
      display: block;
      transition: all 0.3s ease;
    }
    #click:checked ~ ul{
      left: 0;
    }
    #nav ul li{
      width: 100%;
      margin: 40px 0;
    }
    #nav ul li a{
      width: 100%;
      margin-left: -100%;
      display: block;
      font-size: 20px;
      transition: 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }
    #click:checked ~ ul li a{
      margin-left: 0px;
    }
    #nav ul li a.active,
    #nav ul li a:hover{
      background: none;
      color: #F27373;
    }
  }
  @media screen and (min-width: 320px) and (max-width:1034px){
    #nav{
      padding: 0px 0px;
      display:flex;
      width:100%;

      a{
        display:flex;
        flex-direction: row wrap;
      }
    }
  }

  @media (min-width: 1001px) and (max-width: 1025px) {
    #nav{
      padding: 0px 0px;
      display:flex;
      width:100%;

      a{
        display:flex;
        flex-direction: row wrap;
      }
    }

    #nav ul li a{
      width: 100%;
      display: block;
      font-size: 10px;
      transition: 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }
  }
</style>
