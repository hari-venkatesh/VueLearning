
<!-- Basci Usage -->

import { defineAsyncComponent } from 'vue'

const AsyncComp = defineAsyncComponent(() => {
  return new Promise((resolve, reject) => {
    resolve(/* loaded component */)
  })
})

import { defineAsyncComponent } from 'vue'

const AsyncComp = defineAsyncComponent(() =>
  import('./components/MyComponent.vue')
)

app.component('MyComponent', defineAsyncComponent(() =>
  import('./components/MyComponent.vue')
))

<script>
import { defineAsyncComponent } from 'vue'

export default {
  components: {
    AdminPage: defineAsyncComponent(() =>
      import('./components/AdminPageComponent.vue')
    )
  }
}
</script>

<template>
  <AdminPage />
</template>

<!-- Loading and Error States -->

const AsyncComp = defineAsyncComponent({
    loader: () => import('./Foo.vue'),

    loadingComponent: LoadingComponent,

    delay: 200,

    errorComponent: ErrorComponent,
    timeout: 3000
  })
  