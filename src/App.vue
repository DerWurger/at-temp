<script setup lang="ts">
import {computed, ref, watch} from "vue";
import Button from "@/Button.vue";

const title = ref("World!");

const count = ref(-1);

const setCount = (countChild: number) => {
  count.value = countChild;
}
</script>

<template>
  <Button :title="title" @clicked="setCount"></Button>
  <p>Count in child {{count}}</p>
</template>

<style scoped></style>
