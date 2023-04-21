<template>
    <div>
      <h2>Crear Producto</h2>
      <form>
        <div>
          <label for="nombre">Nombre:</label>
          <input type="text" id="nombre" v-model="nombre">
        </div>
        <div>
          <label for="precio">Precio:</label>
          <input type="number" id="precio" v-model="precio">
        </div>
        <div>
          <button @click.prevent="crearProducto">Crear</button>
        </div>
      </form>
    </div>
  </template>

  <script>
  export default {
    data() {
      return {
        nombre: '',
        precio: null
      }
    },
    methods: {
      crearProducto() {
        this.$http.post('/api/products', {
          nombre: this.nombre,
          precio: this.precio
        }).then(response => {
          console.log(response.data)
        }).catch(error => {
          console.log(error)
        })
      }
    }
  }
  </script>
