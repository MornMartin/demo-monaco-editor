<template>
    <div ref="editor" id="editor"></div>
</template>

<script>
import * as monaco from 'monaco-editor';
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted() {
    monaco.editor.create(this.$refs.editor, {
      value: 'console.log("Hello, world")',
      language: 'typescript'
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#editor{
  height: 400px;
}
</style>
