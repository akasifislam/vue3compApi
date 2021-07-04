<template>
  <div class="home"></div>

  <h1>This name is {{ name }} and age is {{ age }}</h1>
  <button @click="handleClick">click me</button>
  <input type="text" v-model="name" />

  <button @click.prevent="age++">Age</button>
</template>

<script>
import { ref } from "@vue/reactivity";
export default {
  name: "Home",

  setup() {
    console.log(this);

    // const p = ref("ami ref er custom data");
    // console.log(p, p.value);
    const name = ref("mastrer man");
    const age = ref(33);

    const handleClick = () => {
      name.value = "ami ki ar bolbo";
      age.value = 22;
    };

    return {
      name,
      age,
      handleClick,
    };
  },
};
</script>
