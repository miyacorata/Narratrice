<template>
  <textarea id="editor"></textarea>
</template>

<script>
import CodeMirror from 'codemirror'
import 'codemirror/lib/codemirror.css'
import 'codemirror/addon/edit/matchbrackets'
import 'codemirror/mode/sparql/sparql'

const defaultCode = 
`PREFIX lily: <https://lily.fvhp.net/rdf/IRIs/lily_schema.ttl#>
PREFIX lilyrdf: <https://lily.fvhp.net/rdf/RDFs/detail/>
PREFIX schema: <http://schema.org/>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX foaf: <http://xmlns.com/foaf/0.1/>

`

export default {
  components: {
    CodeMirror,
  },
  mounted () {
    const editor = document.querySelector('#editor')
    this.editor = CodeMirror.fromTextArea(editor, {
      lineNumbers: true,
      mode: 'sparql',
    })
    this.editor.setValue(defaultCode)
  }
}
</script>

<style>
.CodeMirror {
  border-bottom: solid 1px black !important;
  height: 100px;
  transition: height ease .3s;
}
.CodeMirror:hover{
  height: 80vh;
}
</style>