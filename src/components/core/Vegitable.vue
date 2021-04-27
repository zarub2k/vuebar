<template>
  <li>{{ veg.name }} >> {{ veg.price }}</li>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "Vegitable",
  props: {
    vegitable: {
      type: Object
    },
  },
  setup(props) {
    const veg = reactive(props.vegitable);
    return {
      veg,
    }
  }
}
</script>