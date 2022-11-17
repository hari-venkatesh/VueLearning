
<!-- Conditional Rendering -->

<!-- v-if -->

<h1 v-if="awesome">Hari is awesome!</h1>

<!-- v-else -->

<button @click="awesome = !awesome">Toggle</button>

<h1 v-if="awesome">Hari is awesome!</h1>
<h1 v-else>Yes Of course he is!</h1>

<!-- v-if on template -->

<template v-if="ok">
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
  </template>