<template>
  <div class="home"></div>

  <h1 ref="p">This name is {{ name }} and age is {{ age }}</h1>
  <button @click="handleClick">click me</button>
</template>

<script>
import { ref } from "@vue/reactivity";
export default {
  name: "Home",

  setup() {
    console.log(this);

    const p = ref("ami ref er custom data");
    console.log(p, p.value);
    let name = "mastrer man";
    let age = "26";

    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add("test");
      p.value.textContent = "Amar kono kaj nai nak";
    };

    return {
      name,
      age,
      handleClick,
      p,
    };
  },
};
</script>
