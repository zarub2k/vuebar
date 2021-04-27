<template>
  <div>{{ counter }}</div>
</template>

<script>
import { onMounted, ref } from "vue";
export default {
  name: "Counter",
  setup() {
    let counter = ref(0);
    onMounted(() => {
      setInterval(() => {
        counter.value++;
      }, 1000);
    });

    return {
      counter
    }
  },
}
</script>