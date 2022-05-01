<template>
  <!-- <div class="cards">
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
  <div class="cards">
    <b-container fluid>
      <div>
        <b-row align-h="start">
          <b-col class="contenido" cols="10">
            <b-row>
              <b-col align-self="center" lg="8" cols="8">
                <b-row class="informacion" cols="2">
                  <b-col cols="12">
                    <h1 class="h1-left">{{ titulo }}</h1>
                  </b-col>
                  <b-col cols="12">
                    <p>
                      {{ descripcion }}
                    </p>
                  </b-col>
                  <b-col cols="12">
                    <h3>{{ precio }}</h3>
                  </b-col>
                </b-row>
              </b-col>
              <b-col align-self="center" xs="3" lg="4" cols="4">
                <img :src="img" loading="lazy" alt="" srcset="" />
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
img {
  width: 20vw !important;

  transform: translateX(70%);
  background: transparent !important;
}

.contenido {
  padding: 50px;
  border-color: var(--cardinal);
  border-style: solid;
  border-width: 1px 1px 1px 0px;
}
p {
  font-size: 3vw;
  text-align: left;
}
.h1-left {
  font-size: 10vw !important;

  font-size: 3vw;
  text-align: left;
}
h3 {
  font-size: 4vw !important;
  text-align: left;
}
.informacion {
  transform: translateX(20%) !important;
  width: 130% !important;
}
.cards {
  margin-top: 10% !important;
}
</style>
