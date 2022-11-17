
<!-- The double mustaches -->

<p>Using text interpolation: {{ rawHtml }}</p>
<p>Using v-html directive: <span v-html="rawHtml"></span></p>

<span style="color: red">This should be red.</span>

<!-- Attribute Bindings -->
<!-- The v-bind -->

<div v-bind:id="dynamicId"></div>

<!-- Dynamically Binding Multiple Attribute -->

data() {
  return {
    objectOfAttrs: {
      id: 'container',
      class: 'wrapper'
    }
  }
}

<!-- Directives -->

<p v-if="seen">Now you see me</p>

<a v-bind:href="url"> ... </a>

<a :href="url"> ... </a>

<a v-on:click="doSomething"> ... </a>

<!-- shorthand -->
<a @click="doSomething"> ... </a>

<a v-on:[eventName]="doSomething"> ... </a>

<a @[eventName]="doSomething">

<form @submit.prevent="onSubmit">...</form>