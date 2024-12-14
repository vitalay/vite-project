<template>
  <div class="container-fluid">
    <h1>Hello</h1>
    <keep-alive>
      <component :is="changeComponent"></component>
    </keep-alive>
    
    <button @click="nameComponent = 'One'" class="btn btn-success">ONE</button>
    <hr />
    <button @click="nameComponent = 'Two'" class="btn btn-success">TWO</button>
    <hr />
    <button @click="nameComponent = 'Three'" class="btn btn-success">
      THREE
    </button>
    <hr />
   
     <form @submit.prevent="formSubmit">
      <input type="text" :value="inputOne" @input="inputChangeOne" class="form-control">
      <input 
      type="text" 
      v-model="inputTwo" 
      class="form-control"
      ref="inputRefTwo"
      >
      <br/>
      <hr/>
      <button type="submit" :value="inputTwo" class="btn btn-primary">Отправить</button>
    </form> 

    <FormsBlock></FormsBlock>
    <FormsBlock2></FormsBlock2>
  </div>
</template>

<script>
import BlockContentOne from "./BlockContentOne.vue";
import BlockContentTwo from "./BlockContentTwo.vue";
import BlockContentThree from "./BlockContentThree.vue";
import FormsBlock from "./FormsBlock.vue";
import FormsBlock2 from "./FormsBlock2.vue";

export default {

  data() {
    return {
      inputOne: "",
      inputTwo: "",
      nameComponent: "One",
    };
  },
  computed: {
    changeComponent() {
      return "BlockContent" + this.nameComponent;
    },
  },
  methods: {
    formSubmit() {
      console.log('formSubmit', this.inputOne)
      console.log('formSubmit', this.inputTwo)
      console.log('inputRefTwo', this.$refs.inputRefTwo.value)
    },
     
    inputChangeOne(event) {
      console.log('inputChangeOne', event.target.value)
      this.inputOne = event.target.value
    }
 
  },
 
  components: {
    BlockContentOne,
    BlockContentTwo,
    BlockContentThree,
    FormsBlock,
    FormsBlock2
  }, 
};
</script>

<style></style>
