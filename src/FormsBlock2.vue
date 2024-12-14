<template>
    <form @submit.prevent="formSubmit">
      <h2>Ваша страна</h2>
      <select v-model="Country">
        <option value="rus">Россия</option>
        <option value="ki">Китай</option>
        <option value="tw">Тайвань</option>
        <option value="usa">United States of America</option>
      </select>
      <hr />
      <button type="submit" class="btn btn-primary">Отправить</button>
    </form>
  </template>
  
  <script>
  export default {
    data() {
      return {
        Country: 'tw' // Начальное значение выбранного элемента
      };
    },
    methods: {
      formSubmit() {
        console.log('Выбранная страна:', this.Country);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Ваш CSS */
  </style>
  