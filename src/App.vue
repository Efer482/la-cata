<template>
  <div class="body vh-100" id="app">
    <b-container class="name text-light text-center">
      <b-row align-h="center" class="justify-content-md-center">
        <b-col id="span1" cols="2" align-self="center"> <span></span> </b-col>
        <b-col> <h1>La Cata</h1> </b-col>
        <b-col id="span2" cols="2" align-self="center"> <span></span> </b-col>
      </b-row>
    </b-container>
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <b-card-group deck v-for="(show, index) in productos" :key="index">
      <CardRigth
        v-if="index % 2 == 0"
        :titulo="show.titulo"
        :descripcion="show.texto"
        :img="show.img"
        :precio="show.precio"
      />
      <CardLeft
        v-else
        :titulo="show.titulo"
        :descripcion="show.texto"
        :img="show.img"
        :precio="show.precio"
      />
    </b-card-group>
    <b-container class="name text-light text-center">
      <b-row align-h="center" class="justify-content-md-center">
        <b-col id="span1" cols="2" align-self="center"> <span></span> </b-col>
        <b-col> <h1>La Cata</h1> </b-col>
        <b-col id="span2" cols="2" align-self="center"> <span></span> </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import CardRigth from "./components/CardRigth.vue";
import CardLeft from "./components/CardLeft.vue";

export default {
  name: "App",
  components: {
    CardRigth,
    CardLeft,
  },
  data() {
    return {
      productos: [
        {
          titulo: "Vino Tinto",
          texto:
            "El vino tinto es un tipo de vino procedente mayormente de mostos de uvas tintas, con la elaboración pertinente para conseguir la difusión de la materia colorante que         contienen los hollejos de la uva.",
          precio: "$3000",
          img: require("./img/min/vinoTinto.png"),
        },
        {
          titulo: "Champagne",
          texto:
            "Vinos espumosos producidos exclusivamente de uvas cultivadas, vendimiadas y elaboradas como vino en la región de Champagne, una zona exclusiva delimitada de Francia. La única región del mundo donde se produce exclusivamente este vino espumoso.",
          precio: "$3000",
          img: require("./img/min/champagne.png"),
        },
        {
          titulo: "Queso Dorblu",
          texto:
            "El Dorblu es un queso de leche pasteurizada de vaca, de delicado moho azul, ni muy salado ni muy picante, que nació a principios del pasado siglo en la ciudad alemana de Lauben, en los Alpes de Allgäu",
          precio: "$3000",
          img: require("./img/min/queso.png"),
        },
      ],
    };
  },
};
</script>

<style>
@font-face {
  font-family: Sylfaen Regular;
  src: url(./fonts/Sylfaen_Regular.ttf);
}
:root {
  --black: rgba(0, 0, 0, 1);
  --dove-gray: rgba(112, 112, 112, 1);
  --cardinal: rgba(188, 19, 65, 1);
  --white: rgba(255, 255, 255, 1);

  --font-size-m: 13px;
  --font-size-l: 17px;
  --font-size-xl: 25px;
  --font-size-xxl: 50px;

  --font-family-sylfaen-regular: "Sylfaen Regular";
}

* {
  background: var(--black);
  color: var(--cardinal);
  font-family: var(--font-family-sylfaen-regular);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.name {
  margin: 7vh;
}
h1 {
  font-size: 14vw !important;
  padding: 0% !important;
  margin: 0% !important;
}
span {
  right: 0%;
  display: block;
  background: var(--cardinal) !important;
  border-style: solid !important;
  height: 0px !important;
  border-width: 1px;
  border-color: var(--cardinal) !important;
}
#span1 {
  transform: translateX(50%) !important;
}
#span2 {
  transform: translateX(-50%) !important;
}
</style>
