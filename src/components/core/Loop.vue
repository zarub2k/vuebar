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
    <h3>Loop with subcomponents</h3>
    <ul>
    <Vegitable v-for="vegitable in vegitables" :key="vegitable" :vegitable="vegitable"/>
    </ul>
  </div>
</template>

<script>
import { reactive, ref } from "vue";
import Vegitable from "@/components/core/Vegitable";

export default {
  components: {
    Vegitable,
  },
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