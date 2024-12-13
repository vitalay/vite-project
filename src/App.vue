<template>
  <div class="container-fluid">
    <h1>Hello</h1>
    <keep-alive>
      <BlockContentOne v-if="nameComponent === 'One'" />
      <BlockContentTwo v-else-if="nameComponent === 'Two'" />
      <BlockContentThree v-else />
    </keep-alive>
    <hr />
    <button @click="nameComponent = 'One'" class="btn btn-success">ONE</button>
    <hr />
    <button @click="nameComponent = 'Two'" class="btn btn-success">TWO</button>
    <hr />
    <button @click="nameComponent = 'Three'" class="btn btn-success">THREE</button>
    <hr />
  </div>
</template>

<script>
import BlockContentOne from "./BlockContentOne.vue";
import BlockContentTwo from "./BlockContentTwo.vue";
import BlockContentThree from "./BlockContentThree.vue";

export default {
  data() {
    return {
      nameComponent: "One",
    };
  },
  components: {
    BlockContentOne,
    BlockContentTwo,
    BlockContentThree,
  },
};
</script>

<style></style>
