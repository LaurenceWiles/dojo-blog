<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">updateNinjaOne</button>
    <h2>Reactive</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
    <button @click="updateNinjaTwo">updateNinjaTwo</button>
  </div>
</template>

<script>
import { reactive, ref } from "vue";

// @ is an alias to /src

export default {
  name: "HomeView",
  setup() {
    const ninjaOne = ref({ name: "mario", age: 30 });
    const ninjaTwo = reactive({ name: "luigi", age: 35 });

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40;
    };
    const updateNinjaTwo = () => {
      ninjaTwo.age = 45;
    };
    return { ninjaOne, updateNinjaOne, ninjaTwo, updateNinjaTwo };
  },
};
</script>
