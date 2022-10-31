<template>

  <section class="src-components-container">
    <div id="container">
      <div v-for="(color, index) in squares" :key="index" class="square" :style="{ 'background': color }"
        @click="validateColor(color, index)"></div>

    </div>
  </section>

</template>

<script>

export default {
  name: 'src-components-container',
  props: ["squares", "picked-color"],
  mounted() {

  },
  data() {
    return {

    }
  },
  methods: {
    //Querria usar el index para que el componente padre setee el color a blanco si el square no tiene el color correcto.
    validateColor(color, index) {
      console.log(index)
      if (this.pickedColor == color) {
        console.log("Color correcto")
        this.$emit('winner-found', color)
      } else {
        console.log("Color erroneo")
      }
    }

  },
  computed: {

  }
}


</script>

<style scoped lang="css">
.src-components-container {
  margin: 20px auto;
  max-width: 600px;

}

#container {
  background: #232323; 
  font-family: "Montserrat", "Avenir";
}

.square {
  width: 30%;
  background: blue;
  padding-bottom: 30%;
  float: left;
  margin: 1.66%;
  border-radius: 10%;
  transition: background 0.8s;
  -webkit-transition: background 0.8s;
  -moz-transition: background 0.8s;
}
</style>
