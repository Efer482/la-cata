<template>
  <!-- <div class="cards-rigth">
    <div class="cuadro">
      <img src="../img/vinoTinto.png" alt="" srcset="" />
      <p>
        El vino tinto es un tipo de vino procedente mayormente de mostos de uvas
        tintas, con la elaboración pertinente para conseguir la difusión de la
        materia colorante que contienen los hollejos de la uva
      </p>
      <h3>$3000</h3>
    </div>
  </div> -->
  <div class="cards-rigth">
    <b-container fluid>
      <div>
        <b-row align-h="end">
          <b-col class="contenido-rigth" cols="10">
            <b-row>
              <b-col align-self="center" cols="4">
                <img
                  class="img-rigth"
                  loading="lazy"
                  :src="img"
                  alt=""
                  srcset=""
                />
              </b-col>
              <b-col align-self="center" cols="8">
                <b-row class="informacion-rigth" cols="2">
                  <b-col cols="12">
                    <h1 class="h1-rigth">{{ titulo }}</h1>
                  </b-col>
                  <b-col cols="12">
                    <p class="p-rigth">{{ descripcion }}</p>
                  </b-col>
                  <b-col cols="12">
                    <h3 class="h3-rigth">{{ precio }}</h3>
                  </b-col>
                </b-row>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "CardRigth",
  props: {
    titulo: {
      type: String,
      default: "Click",
    },
    descripcion: {
      type: String,
      default: "Click",
    },
    precio: {
      type: String,
      default: "Click",
    },
    img: {
      type: String,
      default: "Click",
    },
  },
};
</script>
<style>
.img-rigth {
  width: 20vw !important;
  transform: translateX(-70%);
  background: transparent !important;
}

.contenido-rigth {
  padding: 50px;
  border-color: var(--cardinal);
  border-style: solid;
  border-width: 1px 0px 1px 1px;
}
.h1-rigth {
  font-size: 10vw !important;
  text-align: right;
}
.p-rigth {
  font-size: 3vw;
  text-align: right;
}
.h3-rigth {
  font-size: 4vw !important;
  text-align: right;
}
.informacion-rigth {
  transform: translateX(-35%) !important;
  width: 130% !important;
  margin-right: 4% !important;
}
.cards-rigth {
  margin-top: 10% !important;
}
</style>
