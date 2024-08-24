<script>
export default {
  name: 'TarjetaCredito',
  data() {
    return {
      user: {
        titulo: '',
        chip: '',
        numero: '',
        expiracion: '',
        propietario: '',
        tipo: ''
      }
    };
  }
}

</script>

<template>

<div id="app">
      <form>
        <div>
          <label >Título de la tarjeta: </label>
         <input type="text" v-model="user.titulo" >
        </div>

        <div>
          <label>Chip SRC: </label>
          <input type="text" v-model="user.chip">
          
        </div>

        <div>
          <label>Número: </label>
          <input type="text" v-model="user.numero">
        </div>

        <div>
          <label>Fecha de expiración: </label>
          <input type="text" v-model="user.expiracion">
        </div>

        <div>
          <label>Propietario: </label>
          <input type="text" v-model="user.propietario">
          
        </div>

        <div>
          <label>Tipo de tarjeta SRC: </label>
          <input type="text" v-model="user.tipo">
        
        </div>
      </form>

      <div class="carnet">
        <h3> {{user.titulo  }}</h3>
        <img :src="user.chip" alt="" width="40" >
        <div>
          <h2>{{user.numero  }}</h2>
          <span>Fecha Exp: <b>{{user.expiracion  }}</b></span>
        </div>
        <footer>
          <span>{{user.propietario  }}</span>
          <img :src="user.tipo" alt="" width="60" >
        </footer>
      </div>
    </div>
 
</template>

<style scoped>
     
      form {
        padding: 18px;
        border-radius: 20px;
        border: ridge 1px;
        box-shadow: 1px 1px 1px 1px gray;
        font-weight: bold;
        display: flex;
        flex-direction: column;
        gap: 15px;
        justify-content: center;
      }
      form div {
        display: grid;
        grid-template-columns: 100px 200px;
        align-items: center;
        gap: 5px;
      }

      form div label {
        text-align: right;
      }

      .carnet {
        width: 400px;
        height: 230px;
        background: #1c1a1e;
        color: white;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 0px 0px 10px 2px black;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

      h3 {
        font-size: 20px;
      }

      h2 {
        font-size: 30px;
        letter-spacing: 10px;
        margin-bottom: 15px;
        text-shadow: 0px 0px 1px gold;
        font-family: Times;
      }

      b {
        font-size: 16px;
      }

      footer {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        font-weight: bold;
        font-size: 18px;
        text-transform: uppercase;
        font-style: italic;
      }

</style>