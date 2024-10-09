<template>
    <div>
      <h1>Selecciona un Color</h1>
      <select v-model="selectedColor">
        <option disabled value="">Por favor selecciona un color</option>
        <option v-for="color in colors" :key="color" :value="color">{{ color }}</option>
      </select>
      <p :style="{ color: selectedColor }">
        El color seleccionado es: {{ selectedColor }}
      </p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        colors: ['Rojo', 'Verde', 'Azul', 'Amarillo', 'Naranja', 'Violeta'],
        selectedColor: '',
      };
    },
  };
  </script>