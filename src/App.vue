<template>
  <div id="app">123
    <div class="editor">
      <codemirror ref="cmEditor" v-model="code" :options="cmOptions"/>
    </div>123
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import { codemirror } from "vue-codemirror";

export default {
  name: "App",
  components: {
    HelloWorld,
    codemirror
  },
  data() {
    return {
      code: "",
      cmOptions: {
        tabSize: 4,
        mode: "text/javascript",
        lineNumbers: true,
        line: true
      }
    };
  }
};
</script>

<style>
.editor {
  border: 1px solid gray;
}

#app .CodeMirror {
  height: 30px;
  font-family: -apple-system, BlinkMacSystemFont, "Helvetica Neue", Helvetica,
    "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "\5FAE\8F6F\96C5\9ED1",
    Arial, sans-serif;
  font-size: 14px;
  line-height: 1.5;
  color: #606266;
}

#app .CodeMirror-scroll {
  overflow: hidden;
}
</style>
