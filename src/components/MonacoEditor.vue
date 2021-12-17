<script setup>
import * as monaco from "monaco-editor";

defineProps({
  //   msg: String
});

this.monacoInstance = monaco.editor.create(this.$refs["container"], {
  value: this.value,
  ...this.options,
});
</script>

<template>
  <div class="the-code-editor-container" ref="container"></div>
</template>

<style scoped>
</style>
