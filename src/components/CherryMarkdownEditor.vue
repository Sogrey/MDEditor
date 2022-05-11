<template>
    <div id="markdown-container" class="cherry-markdown-editor">
    </div>
</template>

<script>
import Cherry from 'cherry-markdown';
import CherryMermaidPlugin from 'cherry-markdown/dist/addons/cherry-code-block-mermaid-plugin';
import echarts from 'echarts';
import mermaid from 'mermaid';

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

        // 插件注册必须在Cherry实例化之前完成
        Cherry.usePlugin(CherryMermaidPlugin, {
            mermaid, // 传入mermaid引用
            // mermaidAPI: mermaid.mermaidAPI, // 也可以传入mermaid API
            // 同时可以在这里配置mermaid的行为，可参考mermaid官方文档
            theme: 'neutral',
            sequence: { useMaxWidth: false, showSequenceNumbers: true }
        });

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
                echarts,
                mermaid
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
