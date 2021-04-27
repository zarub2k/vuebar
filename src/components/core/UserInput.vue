<template>
  <div>
    <h1>User input example</h1>
    <p> {{ message }}</p>
    <p><button @click="reverse()">Reverse</button></p>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    let message = ref("Tham");
    const reverse = function() {
      message.value = message.value
        .split('')
        .reverse()
        .join('');
    };

    return {
      message,
      reverse,
    }
  },
}
</script>