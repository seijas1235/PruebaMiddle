<template>
  <div>
    <h2>Listado de productos</h2>
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>Nombre</th>
          <th>Descripción</th>
          <th>Precio</th>
          <th>Acciones</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(producto, index) in productos" :key="producto.id">
          <td>{{ producto.id }}</td>
          <td>{{ producto.nombre }}</td>
          <td>{{ producto.descripcion }}</td>
          <td>{{ producto.precio }}</td>
          <td>
            <button @click="editarProducto(producto.id)">Editar</button>
            <button @click="eliminarProducto(index)">Eliminar</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

  <script>
  export default {
    data() {
      return {
        productos: [],
      };
    },
    methods: {
      cargarProductos() {
        // Aquí iría la lógica para cargar los productos desde la API
      },
      editarProducto(id) {
        // Aquí iría la lógica para editar un producto
        console.log(`Editar producto con ID: ${id}`);
      },
      eliminarProducto(index) {
            this.productos.splice(index, 1);
        },
    },
    mounted() {
      this.cargarProductos();
    },
  };
  </script>
