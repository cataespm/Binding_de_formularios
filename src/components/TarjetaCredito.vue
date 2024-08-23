<script>
export default {
  nombre: 'Tarjeta',
  data() {
    return {
      tarjeta: {
        titulotarjeta: '',
        chipsrc: '',
        numero: '',
        fechaexpiracion: '',
        propietario: '',
        tipotarjetasrc: ''
      }
    }
  }
}
</script>
<template>
  <div id="app">
    <form>
      <div>
        <label for="tarjeta-name" class="form-label">Título de la tarjeta</label>
        <input id="tarjeta-name" class="form-control" type="text" v-model="tarjeta.titulotarjeta" />
      </div>

      <div>
        <label for="tarjeta-name" class="form-label">Chip SRC: </label>
        <input id="tarjeta-name" class="form-control" type="text" v-model="tarjeta.chipsrc" />
      </div>

      <div>
        <label for="tarjeta-name" class="form-label">Número: </label>
        <input id="tarjeta-name" class="form-control" type="text" v-model="tarjeta.numero" />
      </div>

      <div>
        <label for="tarjeta-name" class="form-label">Fecha de expiración: </label>
        <input
          id="tarjeta-name"
          class="form-control"
          type="text"
          v-model="tarjeta.fechaexpiracion"
        />
      </div>

      <div>
        <label for="tarjeta-name" class="form-label">Propietario: </label>
        <input id="tarjeta-name" class="form-control" type="text" v-model="tarjeta.propietario" />
      </div>

      <div>
        <label for="tarjeta-name" class="form-label">Tipo de tarjeta SRC: </label>
        <input
          id="tarjeta-name"
          class="form-control"
          type="text"
          v-model="tarjeta.tipotarjetasrc"
        />
      </div>
    </form>

    <div class="carnet">
      <h3>{{ tarjeta.titulotarjeta }}</h3>
      <img width="40" v-bind:src="tarjeta.chipsrc" alt="" />
      <div>
        <h2>{{ tarjeta.numero }}</h2>
        <span
          >Fecha Exp: <b> {{ tarjeta.fechaexpiracion }}</b></span
        >
      </div>
      <footer>
        <span>{{ tarjeta.propietario }}</span>
        <img v-bind:src="tarjeta.tipotarjetasrc" width="60" />
      </footer>
    </div>
  </div>
</template>
<style scoped></style>
