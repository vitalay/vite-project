<template>
       <form @submit.prevent="formSubmit">
        <strong>Где предпочитаете отдыхать</strong>
        <br />
        <label for="1"><input
             class="form-check-input"
             type="checkbox" v-model="rest" value="Кипр" 
             >Кипр</label>
             <br>
        <label for="2"><input
             class="form-check-input" 
             type="checkbox" v-model="rest" value="Греция"
             >Греция</label>
             <br>
        <label for="3"><input
             class="form-check-input"
             type="checkbox" v-model="rest" value="Турция"
             >Турция</label>
             <br>
             <strong>Где предпочитаете отдыхать</strong>
             <br>
             <label for="4"><input
             class="form-check-input"
             type="checkbox" v-model="agree" 
             >Италия</label>
             <br>
             <span>Что предпочитаете на ужин</span>
             <br>
             <label><input
             class="form-check-input"
             type="radio" value="Крабы" v-model="dish" 
             />Крабы</label>
             <br>
             <label><input
             class="form-check-input"
             type="radio" value="Раки" v-model="dish" 
             />Раки</label>
             <br>
             <label><input
             class="form-check-input"
             type="radio" value="Омары" v-model="dish" 
             />Омары</label>
             <br>
             <label><input
             class="form-check-input"
             type="radio" value="Криветки" v-model="dish" 
             />Криветки</label>
             <br>
             <hr>
             <button type="submit" class="btn btn-primary">Отправить</button>
    </form>
</template>

<script>
export default {
data() {
  return {
    rest: [],
    agree: false,
    dish: null
  }
},
methods: {
  formSubmit() {
    console.log('dish', this.dish)
    console.log('rest', this.rest)
    console.log('agree', this.agree)
  }     
}
}
</script>

<style>

</style>