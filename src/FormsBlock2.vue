<template>
  <form v-on:submit.prevent="formSubmit">
 <h2>Ваша страна</h2>
<select name="country">
  <option value="Россия">Россия</option>
  <option selected value="Китай">Китай</option>
  <option value="Тайвань">Тайвань</option>
  <option  value="USA">United States of America</option>
</select>
<hr />
    <button type="submit" class="btn btn-primary">Отправить</button>
  </form>
</template>

<script>
export default {
    data() {
        return {
    }

},
methods: {
    formSubmit() {
        console.log('formSubmit')
    }
}
}

</script>

<style>

</style>