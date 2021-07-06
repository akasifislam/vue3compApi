<template>
  <div class="home"></div>

  <h2>Refs</h2>
  <h1>{{ mastermanOne.name }} - {{ mastermanOne.age }}</h1>
  <button @click="updateAsifOne">Update</button>
  <h2>Reactive</h2>
  <h1>
    name: {{ mastermanTwo.name }} and age {{ mastermanTwo.age }} -
    {{ masterTwo }}
  </h1>
  <button @click="updateAsifTwo">Update</button>
  <!-- <button @click="handleClick">click me</button>
  <input type="text" v-model="name" />

  <button @click.prevent="age++">Age</button> -->
</template>

<script>
import { reactive, ref } from "@vue/reactivity";
export default {
  name: "Home",

  setup() {
    const mastermanOne = ref({ name: "muhammad asif ul islam", age: 26 });
    const mastermanTwo = reactive({ name: "ema watson", age: 25 });

    const masterOne = ref("master One");
    const masterTwo = ref("master Two");

    const updateAsifOne = () => {
      mastermanOne.value.name = "zjskhfkjs rsfguiwer";
      mastermanOne.value.age = 40;
    };
    const updateAsifTwo = () => {
      mastermanTwo.name = "dfzgdfg";
    };

    return {
      mastermanOne,
      updateAsifOne,
      mastermanTwo,
      updateAsifTwo,
      masterOne,
      masterTwo,
    };

    // ============================================================

    // console.log(this);

    // const p = ref("ami ref er custom data");
    // console.log(p, p.value);
    // const name = ref("mastrer man");
    // const age = ref(33);

    // return {
    //   name,
    //   age,
    //   handleClick,
    // };
  },
};
</script>
