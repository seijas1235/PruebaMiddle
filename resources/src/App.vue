<template>
    <div>
      <h1>Productos</h1>
      <ListaProductos />
      <FormProductos />
    </div>
  </template>

  <script>
  import ListaProductos from './listaProductos.vue'
  import FormProductos from './formProductos.vue'

  export default {
    components: {
      ListaProductos,
      FormProductos,
    },
  }
  </script>
