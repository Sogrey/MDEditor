<template>
    <div id="markdown-container" class="cherry-markdown-editor">
    </div>
</template>

<script>
import Cherry from 'cherry-markdown';
import echarts from 'echarts';

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
        // new Cherry({
        //   id: 'markdown-container',
        //   value: "# Hello",
        // });

        new Cherry({
            id: 'markdown-container',
            value: '# welcome to cherry editor!',
            editor: {
                theme: 'default',
                height: '100%',
                defaultModel: 'edit&preview',
            },
            toolbars: {
                theme: 'dark', // light or dark                                                                            
                toolbar: ['bold', 'italic', 'strikethrough', '|', 'color', 'header', '|', 'list', { insert: ['image', 'audio', 'video', 'link', 'hr', 'br', 'code', 'formula', 'toc', 'table', 'line-table', 'bar-table', 'pdf', 'word',], }, 'graph', 'togglePreview', '|', 'settings'],
                bubble: ['bold', 'italic', 'strikethrough', 'sub', 'sup', '|', 'size', 'color'], // array or false                 
                float: ['h1', 'h2', 'h3', '|', 'size', 'color', '|', 'checklist', 'quote', 'quickTable', 'code'], // array or false         
                customMenu: {
                }
            },
            externals: {
                echarts
            },
            // fileUpload(file, callback) {
            //     callback(url);
            // },
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
