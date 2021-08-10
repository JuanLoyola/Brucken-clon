<template>
  <div class="container">
    <div class="slider">
      <button @click="next" class="next">
          <i class="fas fa-chevron-left"></i>
        </button>
    <div class="info-bottom" id="slide">
      <div class="card" v-for="(item, index) in items" :key="index">
        <div class="imgBox">
          <img class="image" style="width:100%" :src="item.src" alt="product image">
        </div>
          <p class="title">{{item.title}}</p>
          <p class="place"><i class="fas fa-map-marker-alt"></i> {{item.place}}</p>
          <p class="info">{{item.info}}</p>
          <div class="btnBox">
            <button class="btn"><span class="plus">+</span>Visitar ahora</button>
          </div>
      </div>
    </div>
      <button @click="previous" class="prev">
          <i class="fas fa-chevron-right"></i>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data () {
    return {
      count: 0,
      items: [
        {
          src: require('../assets/bck8_2.jpg'),
          title: 'Departamento en venta',
          place: 'Centro, Santa Fe',
          info: 'Venta de departamento 2 DORMITORIOS en Centro, Santa Fe. Departamento céntrico en Edificio de categoria'
        },
        {
          src: require('../assets/bck10_2.jpg'),
          title: 'Departamento en venta',
          place: 'Centro, Santa Fe',
          info: 'Venta de departamento 2 DORMITORIOS en Centro, Santa Fe. Departamento céntrico en Edificio de categoria'
        },
        {
          src: require('../assets/bck65_2.jpg'),
          title: 'Departamento en venta',
          place: 'Centro, Santa Fe',
          info: 'Venta de departamento 2 DORMITORIOS en Centro, Santa Fe. Departamento céntrico en Edificio de categoria'
        },
        {
          src: require('../assets/bck79_2.jpg'),
          title: 'Departamento en venta',
          place: 'Centro, Santa Fe',
          info: 'Venta de departamento 2 DORMITORIOS en Centro, Santa Fe. Departamento céntrico en Edificio de categoria'
        },
        {
          src: require('../assets/bck10_2.jpg'),
          title: 'Departamento en venta',
          place: 'Centro, Santa Fe',
          info: 'Venta de departamento 2 DORMITORIOS en Centro, Santa Fe. Departamento céntrico en Edificio de categoria'
        },
        {
          src: require('../assets/bck65_2.jpg'),
          title: 'Departamento en venta',
          place: 'Centro, Santa Fe',
          info: 'Venta de departamento 2 DORMITORIOS en Centro, Santa Fe. Departamento céntrico en Edificio de categoria'
        },
        {
          src: require('../assets/bck79_2.jpg'),
          title: 'Departamento en venta',
          place: 'Centro, Santa Fe',
          info: 'Venta de departamento 2 DORMITORIOS en Centro, Santa Fe. Departamento céntrico en Edificio de categoria'
        }
      ],
      frame: 2
    }
  },
  methods: {
    next () {
      this.count--
      this.scroll('previous')
    },
    previous () {
      this.count++
      this.scroll('next')
    },
    scroll (position) {
      const el = document.getElementById('slide')
      let pos = 0
      const id = setInterval(frame, 5)
      const num = this.items.length - this.frame
      const width = 250
      const resize = num * width
      const check = position === 'reset' ? resize : width
      function frame () {
        if (pos === check) {
          clearInterval(id)
        } else {
          pos += 5
          if (position === 'next') {
            el.scrollLeft += 5
          } else {
            el.scrollLeft -= 5
          }
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  margin-bottom: 30px;
  .slider {
    width: 60%;
    height: 600px;
    margin-top: 20px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;

    button {
      font-size: 50px;
      top: calc(50% - 20px);
      border: none;
      color: #333;
      background: none;
      opacity: .3;
    }
    button:focus,
    button:hover {
      outline: none;
      cursor: pointer;
      opacity: .8;
    }

    .prev,
    .next,
    i {
      font-size: 50px;
    }
    .info-bottom {
      width: 100%;
      margin: 30px 0;
      display: flex;
      justify-self: center;
      align-self: center;
      flex-flow: row nowrap;
      overflow: hidden;
      .card {
        width: 340px;
        height: 550px;
        text-align: start;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: flex-start;
        margin: 10px 10px;
        color: #868686;
        .imgBox {
          width: 340px;
          .image {
            width: 100%;
            height: 300px;
            object-fit: cover;
          }
        }

        .title {
          color: #928986;
          font-size: 1.4rem;
          font-weight: bold;
        }

        .btn {
          font-size: 1rem;
          font-weight: 600;
          text-transform: uppercase;
          opacity: 1;

          .plus {
            width: 40px;
            background: #a5d7d5;
            height: 40px;
            color: #fff;
            font-size: 24px;
            border-radius: 40px;
            text-align: center;
            line-height: 40px;
            margin-right: 10px;
            display: inline-block;
          }
        }

        .btn:hover {
          color: #a5d7d5;
        }
      }

      .card i {
        font-size: 1rem;
      }
    }
  }
}
@media (max-width: 768px) {
  .container {
    width: 100%;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    margin-bottom: 30px;
    #slide {
      display: flex;
      overflow: hidden;
      justify-content: space-between;
      align-items: flex-start;
    }
    .slider {
      width: 700px;
      margin-top: 20px;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      button {
          height: 40px;
          width: 50px;
          top: calc(50% - 20px);
          border: none;
          color: #93c0dc;
          background: none;
        }
        button:focus,
        button:hover {
          outline: none;
          cursor: pointer;
        }
      .info-bottom {
        width: 600px;
        margin: 30px 0;
        display: flex;
        justify-self: center;
        align-self: center;
        flex-flow: row nowrap;
        .card {
          .imgBox {
            width: 180px;
          }
        }
      }
    }
  }
}

@media (max-width: 767px) {
  .container {
    width: 100%;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    margin-bottom: 30px;
    #slide {
      display: flex;
      overflow: hidden;
      justify-content: space-between;
      align-items: flex-start;
    }
    .slider {
      width: 330px;
      margin-top: 20px;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      button {
          height: 40px;
          width: 50px;
          top: calc(50% - 20px);
          border: none;
          color: #93c0dc;
          background: none;
        }
        button:focus,
        button:hover {
          outline: none;
          cursor: pointer;
        }
      .info-bottom {
        width: 330px;
        margin: 30px 0;
        display: flex;
        justify-self: center;
        align-self: center;
        flex-flow: row nowrap;
        .card {
          height: 560px;
          .imgBox {
            width: 180px;
          }
        }
      }
    }
  }
}
</style>
