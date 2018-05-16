## VUE TEMPLATE SYSTEM

# Interpolations with Mustache Syntax (curly braces)
- TEXT: The mustache tag will be replaced by the value property on the corresponding data object
```
<h2> {{ a }} </h2>
```
- RAW HTML: Use the span v-html syntax. When including HTML in an object wrap it in ``<span style="color:red">This Should be red.</span>``.
```
<p>Using mustaches: {{ rawHtml }}</p>
<p>Using v-html directive: <span v-html="rawHtml"></span></p>
```
- HTML ATTRIBUTES: mustaches cannot be used, use the v-bind direction
```
<div v-bind:id="dynamicId"></div>
```
- JAVASCRIPT EXPRESSIONS: free to write any javascript here, only one single expression
```
{{ number + 1 }}
{{ ok ? 'YES' : 'NO' }}
{{ message.split('').reverse().join('') }}
<div v-bind:id="'list-' + id"></div>
```
