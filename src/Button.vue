<script setup lang="ts">
import {ref} from "vue";

interface Props {
  title?: string;
}

const props = withDefaults(defineProps<Props>(), {
  title: 'Hello'
});
const emit = defineEmits<{
  (e: 'clicked', count: number): void
}>();

const count = ref(0)

const clicked = () => {
  count.value++;
  emit('clicked', count.value);
}
</script>

<template>
  <div>
    <h1>{{props.title}}</h1>
    <button @click="clicked" title="">Clicked {{count}}</button>
  </div>
</template>

<style scoped>

</style>