<template>
  <h3>{{ xiang.raw() }}</h3>
</template>

<script lang="ts">
import { ref, defineComponent } from "vue";
import { Xiang } from "./xiang";

export default defineComponent({
  name: "Xiangqi",
  props: {
    fen: {
      type: String,
      required: true,
    },
  },
  setup: (props) => {
    const xiang = new Xiang(props.fen);
    return {
      xiang,
    };
  },
});
</script>

<style scoped></style>
