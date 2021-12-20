<script>
import * as monaco from "monaco-editor";
// import 'monaco-editor/esm/vs/basic-languages/javascript/javascript.contribution';
// import 'monaco-editor/esm/vs/editor/contrib/find/findController.js';

defineProps({
  msg: String,
});
console.log(monaco);

// const monacoInstance = monaco.editor.create(document.getElementById("monaco"));
// const monacoInstance = monaco.editor.create(document.getElementById("monaco"), {
//   value: `console.log("hello,world")`,
//   language: "javascript",
// });
// // monacoInstance.dispose();//使用完成销毁实例
</script>

<template>
  <div id="monaco-editor"></div>
</template>

<style scoped>
#monaco {
  width: 100vw;
  height: 100vh;
  margin: 0;
  padding: 0;
}
</style>
