<template>
  <div class="home">
    <p ref="p">My name is {{ name }} and I am {{ age }} years old.</p>
    <button @click="handleClick">Click Me</button>
  </div>
</template>

<script>
import { ref } from "vue";

// @ is an alias to /src

export default {
  name: "HomeView",
  setup() {
    const p = ref(null);

    let name = "mario";
    let age = 30;

    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add("test");
      p.value.textContent = "hello ninjas";
    };

    return { name, age, handleClick, p };
  },
};
</script>
