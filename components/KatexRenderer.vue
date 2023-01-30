<template>
  <div class="content">
    <div v-html="htmlString"></div>
  </div>
</template>

<script lang="ts" setup>
import katex from 'katex';

const props = defineProps<{
  content: string;
}>();

const htmlString = katex.renderToString(props.content);
</script>
