<template>
    <CherryMarkdownEditor />
</template>

<script>
import CherryMarkdownEditor from './components/CherryMarkdownEditor.vue'
export default {
    name: 'App',
    components: {
        CherryMarkdownEditor
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    width: 100vw;
    height: 100vh;
    margin: 0;
    padding: 0;
}
</style>
