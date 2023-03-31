<template>
    <v-select
      v-model="selectedItem"
      :items="options"
      label="Selecciona una opción"
      solo-inverted
      hide-details
      item-text="label"
      item-value="value"
      :filter="customFilter"
    />
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedItem: null,
        options: [
          { label: 'Opción 1', value: 1 },
          { label: 'Opción 2', value: 2 },
          { label: 'Opción 3', value: 3 },
          { label: 'Opción 4', value: 4 },
          { label: 'Opción 5', value: 5 },
        ],
      };
    },
    methods: {
      customFilter(item, queryText, itemText) {
        // Este método se llama para filtrar las opciones en función del texto ingresado en el input
        const searchText = queryText.toLowerCase();
        const optionText = itemText.toLowerCase();
        return optionText.includes(searchText);
      },
    },
  };
  </script>
  