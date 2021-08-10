<template>
  <div class="container">
    <div class="footer-top">
      <div class="col">
        <div class="imgBox">
          <img src="@/assets/logo.png" alt="logo" class="logo">
        </div>
        <p class="info">Un tejido de profesionales de diferentes especialidades, asociados para prestar servicios a medida a compradores y vendedores</p>

        <div class="social">
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-instagram"></i>
          <i class="fab fa-youtube"></i>
        </div>
      </div>

      <div class="col">
        <h1 class="title">Contacto</h1>

        <p><i class="fas fa-map-marker-alt"></i> Moreno 2308 piso 9 of. A, Santa Fe, Capital</p>
        <p><i class="fas fa-phone"></i> 549 34 2547 7883</p>
        <p><i class="fas fa-envelope"></i> info@brucken.com.ar</p>
      </div>

      <div class="col">
        <h1 class="title">Búsquedas rápidas</h1>

        <ul class="row">
          <li>Ventas</li>
          <li>Alquileres</li>
          <li>Casas</li>
          <li>Departamentos</li>
          <li>Locales</li>
          <li>Quintas</li>
        </ul>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="container">
        <div class="left">Provisto por Xintel. Perteneciente a Amaira</div>
        <div class="right">
          <ul class="options">
            <li class="link">Propiedades</li>
            <li class="link">Compradores</li>
            <li class="link">Vendedores</li>
            <li class="link">Sobre nosotros</li>
            <li class="link">Blog</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 100%;
  background: #786d69;
  color: #e0dddc;
  margin-top: 50px;
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: center;

  .footer-top {
    width: 100%;
    padding: 10px 0 30px;
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-items: center;
    border-bottom: 1px solid #9a928f;

    .col {
      width: 410px;
      height: 200px;
      display: flex;
      flex-flow: column nowrap;
      justify-content: space-evenly;
      align-items: flex-start;
      text-align: start;
      margin: 0 20px;

      .imgBox {
        width: 200px;

        .logo {
          width: 100%;
          height: 40px;
        }
      }

      .info {
        width: 400px;
      }

      .fab {
        width: 30px;
        font-size: 1rem;
        cursor: pointer;
      }

      .fas {
        font-size: 1rem;
      }

      .title {
        margin: 0;
        font-size: 18px;
        font-weight: 600;
        padding-bottom: 10px;
        margin-bottom: 40px;
        position: relative;
        color: #fff;
        line-height: 1.2;
        text-transform: uppercase;
      }

      .title:after {
        content: "";
        background: #fff;
        width: 55px;
        height: 3px;
        position: absolute;
        bottom: 0;
        left: 0;
      }

      .row {
        width: 270px;
        display: flex;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
      }

      .row li {
        display: inline-block;
        flex: 50%;
        padding: 0 15px 15px 0;
        cursor: pointer;
      }

    }
  }

  .footer-bottom {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px 0 30px;

    .container {
      width: 70%;
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      .options {
        width: 550px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        list-style-type: none;

        .link {
          cursor: pointer;
        }
      }
    }
  }
}

@media screen and (max-width: 500px) {
  .container {
    width: 100%;
    height: 100%;
    background: #786d69;
    color: #e0dddc;
    margin-top: 120px;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;

    .footer-top {
      width: 100%;
      padding: 10px 0 20px;
      display: flex;
      flex-flow: column nowrap;
      justify-content: center;
      align-items: center;
      border-bottom: 1px solid #9a928f;

      .col {
        width: 250px;
        height: 220px;
        display: flex;
        flex-flow: column nowrap;
        justify-content: space-evenly;
        align-items: flex-start;
        text-align: start;
        margin: 0 10px;

        .imgBox {
          width: 150px;

          .logo {
            width: 100%;
            height: 40px;
          }
        }

        .info {
          width: 250px;
        }

        .fab {
          width: 30px;
          font-size: 1rem;
          cursor: pointer;
        }

        .fas {
          font-size: 1rem;
        }

        .title {
          margin: 0;
          font-size: 18px;
          font-weight: 600;
          padding-bottom: 10px;
          margin-bottom: 40px;
          position: relative;
          color: #fff;
          line-height: 1.2;
          text-transform: uppercase;
        }

        .title:after {
          content: "";
          background: #fff;
          width: 55px;
          height: 3px;
          position: absolute;
          bottom: 0;
          left: 0;
        }

        .row {
          width: 260px;
          display: flex;
          align-items: center;
          flex-wrap: wrap;
        }

      }
    }

    .footer-bottom {
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 10px 0 30px;

      .container {
        width: 100%;
        height: 200px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;

        .options {
          width: 100%;
          display: flex;
          flex-direction: column;

          .link {
            margin: 5px 0;
          }
        }
      }
    }
  }
}

@media screen and (min-width: 768px) and (max-width: 1000px) {
  .container {
    width: 100%;
    height: 100%;
    background: #786d69;
    color: #e0dddc;
    margin-top: 70px;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;

    .footer-top {
      width: 100%;
      padding: 10px 0 20px;
      display: flex;
      flex-flow: row nowrap;
      justify-content: center;
      align-items: center;
      border-bottom: 1px solid #9a928f;

      .col {
        width: 300px;
        height: 200px;
        display: flex;
        flex-flow: column nowrap;
        justify-content: space-evenly;
        align-items: flex-start;
        text-align: start;
        margin: 0 10px;

        .imgBox {
          width: 150px;

          .logo {
            width: 100%;
            height: 40px;
          }
        }

        .info {
          width: 250px;
        }

        .fab {
          width: 30px;
          font-size: 1rem;
          cursor: pointer;
        }

        .fas {
          font-size: 1rem;
        }

        .title {
          margin: 0;
          font-size: 18px;
          font-weight: 600;
          padding-bottom: 10px;
          margin-bottom: 40px;
          position: relative;
          color: #fff;
          line-height: 1.2;
          text-transform: uppercase;
        }

        .title:after {
          content: "";
          background: #fff;
          width: 55px;
          height: 3px;
          position: absolute;
          bottom: 0;
          left: 0;
        }

        .row {
          width: 260px;
          display: flex;
          align-items: center;
          flex-wrap: wrap;
        }

      }
    }

    .footer-bottom {
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 10px 0 30px;

      .container {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-around;

        .options {
          width: 100%;
          display: flex;
          flex-direction: column;

          .link {
            margin: 5px 0;
          }
        }
      }
    }
  }
}
</style>
