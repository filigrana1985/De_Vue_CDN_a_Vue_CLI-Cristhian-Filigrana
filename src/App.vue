<template>
  <div>
    <table>
      <tr>
        <th>Nombre</th>
        <th>Edad</th>
        <th>Correo electrónico</th>
      </tr>
      <row-component v-for="item in data" :key="item.id" :row-data="item"></row-component>
    </table>
  </div>
</template>

<script>
  import RowComponent from './components/RowComponent.vue';

  export default {
    name:'app',
    components: {
      RowComponent,
    },
    data() {
      return {
        data: [
          { id: 1, nombre: 'Juan', edad: 25, correo: 'juan@example.com' },
          { id: 2, nombre: 'María', edad: 30, correo: 'maria@example.com' },
          { id: 3, nombre: 'Pedro', edad: 28, correo: 'pedro@example.com' }
        ]
      };
    }
  };
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
#table {
    border-collapse: collapse;
    width: 100%;
  }

  th, td {
    border: 1px solid black;
    padding: 8px;
    text-align: left;
  }
</style>
