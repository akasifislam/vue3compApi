<template>
  <div class="home">
    <h1>Home</h1>
      <input type="text" v-model="search">
      <p>search term - {{ search }} </p>
      <ul v-for="name in machingNames" :key="name.id">
        <li>{{ name }} </li> 
      </ul>
  </div>
</template>

<script>
import { computed, ref , watch, watchEffect } from "vue";
export default {
  name: "Home",

  setup() {
    const search = ref("")
    const names = ref(['morgan','massi','trump','azam','malik','ronaldo']);

    watch(search , () =>{
      console.log('watch function run');
    })


    watchEffect(() => {
      console.log('watch effect function run',search.value);
    })




    const machingNames = computed(() =>{
      return names.value.filter((name) => name.includes(search.value))
    })


    return {
      names,
      search,
      machingNames
    };
  },
};
</script>
