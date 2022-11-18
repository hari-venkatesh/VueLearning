
<!-- Component Registration -->

<!-- Global Registration -->

import { createApp } from 'vue'

const app = createApp({})

app.component(
  // the registered name
  'MyComponent',
  // the implementation
  {
    /* ... */
  }
)

import MyComponent from './App.vue'

app.component('MyComponent', MyComponent)

app
  .component('ComponentA', ComponentA)
  .component('ComponentB', ComponentB)
  .component('ComponentC', ComponentC)

  <!-- this will work in any component inside the app -->

<ComponentA/>
<ComponentB/>
<ComponentC/>

<!-- Local Registration -->

<script>
import ComponentA from './ComponentA.vue'

export default {
  components: {
    ComponentA
  }
}
</script>

<template>
  <ComponentA />
</template>

export default {
    components: {
      ComponentA: ComponentA
    }
    // ...
  }
  