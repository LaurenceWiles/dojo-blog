<template>
  <div class="home">
    <p>My name is {{ name }} and I am {{ age }} years old.</p>
    <button @click="handleClick">Click Me</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "HomeView",
  setup() {
    console.log("setup");

    let name = "mario";
    let age = 30;

    const handleClick = () => {
      console.log("you clicked me");
    };

    return { name, age, handleClick };
  },
};
</script>
