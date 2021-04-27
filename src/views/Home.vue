<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <Counter />
    <UserInput />
    <TwowayBinding />
    <Conditional />
    <Loop />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld";
import Counter from "@/components/core/Counter.vue";
import UserInput from "@/components/core/UserInput";
import TwowayBinding from "@/components/core/TwowayBinding";
import Conditional from "@/components/core/Conditional";
import Loop from "@/components/core/Loop";

export default {
  name: "Home",
  components: {
    Counter,
    UserInput,
    TwowayBinding,
    Conditional,
    Loop,
  },
};
</script>
