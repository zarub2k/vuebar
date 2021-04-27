<template>
  <div>
    <h1>Twoway binding example</h1>
    <p> {{ message }}</p>
    <p><input type="text" v-model="message"></p>
    <p><button @click="reverse()">Reverse</button></p>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "TwowayBinding",
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