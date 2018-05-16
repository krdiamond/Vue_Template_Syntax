# VUE TEMPLATE SYSTEM

## Interpolations with Mustache Syntax (curly braces)
- TEXT: The mustache tag will be replaced by the value property on the corresponding data object.
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
```

## Directives
Special attributes using the `v-` prefix.
Reactively applies side effects to the DOM when the value changes
  - EX: v-if directive removes/inserts the <p> element based on the truthiness of the value "seen".
  ```
  <p v-if="seen">Now you see me</p>
  ```
- ARGUMENTS: denoted by a colon
  ```
  <a v-on:click="doSomething"> ... </a>
  ```
- MODIFIERS: denoted by a dote, indicate that a directive should be bound in a special way
  ```
  <form v-on:submit.prevent="onSubmit"> ... </form> === event.preventDefault()
  ```
