<template>
  <div>
    <h2>Loop example</h2>
    <ul>
      <li v-for="fruit in fruits" :key="fruit">{{ fruit }}</li>
    </ul>
    <h3>Reactive loop</h3>
    <ul>
      <li v-for="vegitable in vegitables" :key="vegitable">
        {{ vegitable.name }} - {{ vegitable.price }}
      </li>
    </ul>
  </div>
</template>

<script>
import { reactive, ref } from "vue";

export default {
  setup() {
    const fruits = ref(["Apple", "Banana", "Orange"]);
    const vegitables = reactive([
      { name: "Brinjal", price: 25 },
      { name: "Tomato", price: 10 }
    ]);

    return {
      fruits,
      vegitables,
    }
  },
}
</script>