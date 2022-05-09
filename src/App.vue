<template>
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <CherryMarkdownEditor />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import CherryMarkdownEditor from './components/CherryMarkdownEditor.vue'
export default {
    name: 'App',
    components: {
        // HelloWorld,    
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
    minWidth: 500px;
    minHeight: 600px;
}
</style>
