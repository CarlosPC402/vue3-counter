<script>
  import Logo from "./assets/logo.svg"
  // import Logo2 from "./assets/logo.svg"

  export default{
    data:() => ({
      Logo: Logo
      ,Contador:10
    })
    ,methods:{
      saludar(){
        console.log("hola");
      }
      ,incrementar(){
        this.Contador++;
      }
      ,decrementar(){
        this.Contador--;
      }
      ,reiniciar(){
        this.Contador=10;
      }
    }
  };
  // export default {
  //   data() {
  //     return {
  //       Logo: Logo
  //       // ,LogoTest:Logo2
  //       ,Contador:200
  //     }
  //   }
  // }
</script>

<template>
  <div class="container">
    <img :src="Logo" alt="Logo vue" width="125" height="125">
    <small><h1>Hola mundo desde Vue.js 3</h1></small>
    <!-- <img :src="LogoTest" alt="Logo vue"> -->
    <hr>
    <h2>Contador: {{ Contador }}</h2>
    <button @click="incrementar()">+1</button>
    <button v-on:click="decrementar()">-1</button>
    <button @click="reiniciar()">Reset</button>
  </div>
</template>

<!-- socoped = solo aplica para este archivo los estilos -->
<style scoped>
  .container {
    color: black;
    text-align: center;
  }

  small{
    color: #666;
  }

  h1{
    font-weight: bolder;
  }

  h2{
    font-size: 2.5rem;
  }

  button{
    cursor: pointer;
    font-size: 1.5rem;
    margin: 0px 6px;
  }
</style>


