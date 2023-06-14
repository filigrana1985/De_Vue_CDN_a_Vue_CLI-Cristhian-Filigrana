<template>
   
    <tr>
      <td>{{ rowData.nombre }}</td>
      <td>{{ rowData.edad }}</td>
      <td>{{ rowData.correo }}</td>
    </tr>
  </template>
  
  <script>
    export default {
      props: {
        rowData: {
          type: Object,
          required: true
        }
      }
    };
  </script>
  
  