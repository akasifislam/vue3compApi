<template>
  <div class="home"></div>

  <h1>My name is {{ name }} and age is {{ age }}</h1>
  <button @click="handleClick">click me</button>
</template>

<script>
export default {
  name: "Home",

  setup() {
    let name = "mastrer man";
    let age = "26";

    const handleClick = () => {
      console.log("you click me");
    };

    return {
      name,
      age,
      handleClick,
    };
  },
};
</script>
