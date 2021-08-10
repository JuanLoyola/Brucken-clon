<template>
  <div class="container">
    <h2 class="title">Buscador de propiedades</h2>
    <form class="form">
      <div class="form-row">
        <p class="options">
          <select class="label" id="barrio" name="barrio">
            <option value="All">Barrio</option>
            <option value="Palermo">Palermo</option>
            <option value="Recoleta">Recoleta</option>
            <option value="Belgrano">Belgrano</option>
            <option value="Colegiales">Colegiales</option>
          </select>
        </p>

        <p class="options">
          <select class="label" id="type" name="type">
            <option value="Type">Tipo</option>
            <option value="Palermo">Casa</option>
            <option value="Recoleta">Departamento</option>
            <option value="Belgrano">Ph</option>
            <option value="Colegiales">Duplex</option>
          </select>
        </p>
      </div>

      <div class="form-row">
        <p class="options">
          <select class="label rooms" id="rooms" name="rooms">
            <option value="All">Habitaciones</option>
            <option value="Mono">1 Ambiente</option>
            <option value="Duo">2 Ambientes</option>
            <option value="Triple">3 Ambientes</option>
            <option value="Cuadra">4 Ambientes</option>
          </select>
        </p>

        <p class="form-row">
          <input class="price" id="from" name="from" placeholder="Desde"/>
          <input class="price" id="to" name="to" placeholder="Hasta"/>
        </p>
      </div>

      <input class="direction" id="direction" name="direction" placeholder="Dirección exacta"/>

      <div class="btn-box">
        <button type="submit" class="button">Buscar</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'SearchBox'
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  .title {
    font-size: 2.4rem;
    text-transform: uppercase;
    color: #786d69;
    margin-top: 20px;
  }

  .form {
    width: 740px;
    height: 300px;
    font-size: 1rem;
    background: #786d69;
    margin-top: 50px;
    padding: 30px 40px;
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;

    &-row {
      width: 100%;
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      .price {
        width: 165px;
        border: none;
        background: none;
        color: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 10px 25px;
        border-bottom: 1px solid #a19996;
        cursor: pointer;
      }
      .price::placeholder {
        color: #fff;
        font-size: 1rem;
      }
    }

    .direction {
      width: 98%;
      height: 30px;
      border: none;
      background: none;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 10px 15px;
      margin-top: 10px;
      border-bottom: 1px solid #a19996;
      cursor: pointer;
    }
      .direction::placeholder {
      color: #fff;
      font-size: 1rem;
    }

    .options {
      width: 450px;
      color: #fff;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 5px 10px;
      margin: 0 10px;
      border-bottom: 1px solid #a19996;
      cursor: pointer;

      .label {
        width: 100%;
        height: 35px;
        border: none;
        background: none;
        color: #fff;
        font-size: 1rem;
        cursor: pointer;

      }

      .label option {
        color: #333;
      }

      .rooms {
        width: 290px;
      }
    }

    .btn-box {
      width: 100%;
      display: flex;
      justify-content: flex-end;
      padding-top: 20px;

      .button {
        color: #fff;
        font-weight: bold;
        text-decoration: none;
        text-transform: uppercase;
        padding: 12px 25px;
        border-radius: 5px;
        border: none;
        background: #a5d7d5;
        cursor: pointer;
      }

      .button:hover {
        background: #a2efdf;
      }
    }

  }
}

@media (max-width: 767px) {
  .container {
    height: 100%;
    .form {
      width: 320px;

      &-row {
      width: 100%;
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      .price {
        width: 50%;
        border: none;
        background: none;
        color: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 10px 0px;
        border-bottom: 1px solid #a19996;
        cursor: pointer;
      }
      .price::placeholder {
        color: #fff;
        font-size: 0.6rem;
      }
    }

    .direction {
      width: 90%;
      height: 30px;
      border: none;
      background: none;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 30px 15px;
      border-bottom: 1px solid #a19996;
    }
      .direction::placeholder {
      color: #fff;
      font-size: 1rem;
    }

    .options {
        width: 150px;
        color: #fff;
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 5px 10px;
        margin: 0 10px;
        border-bottom: 1px solid #a19996;
        cursor: pointer;

        .rooms {
          width: 90px;
        }
      }
    }
  }
}
</style>
