<template>
  <div class="content">
    <root />
  </div>
</template>

<script lang="ts" setup>
import katex from 'katex';

const props = defineProps<{
  content: string;
}>();

const root = defineComponent({
  template: katex.renderToString(props.content),
});
</script>
