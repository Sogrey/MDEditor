<template>
  <div id="markdown-container" class="cherry-markdown-editor">
  </div>
</template>

<script>
import Cherry from 'cherry-markdown';

export default {
  name: 'CherryMarkdownEditor',
  // props: {
  //   code: String
  // },
  components: {
    // Cherry
  },
  data() {
    return {};
  },
  mounted() {
    new Cherry({
      id: 'markdown-container',
      value: "# Hello",
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cherry-markdown-editor {
  width: 100vw;
  height: 100vh;
  margin: 0;
  padding: 0;
}
</style>
