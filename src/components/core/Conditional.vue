<template>
  <div>
    <h1>Conditional example</h1>
    <h3>Seen {{ seen }} </h3>
    <h4 v-if="seen">Show</h4>
    <h4 v-else>Not true</h4>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Conditional",
  setup() {
    let seen = ref(true);
    setInterval(() => {
      if (seen.value == true) {
        seen.value = false;
      } else {
        seen.value = true;
      }
    }, 1000)
    return {
      seen,
    }
  },
}
</script>