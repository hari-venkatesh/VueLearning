
<!-- App Creation -->

import { createApp } from 'vue'

<!-- Root Component -->

import App from './App.vue'

const app = createApp({
    
})

<!-- Mounting App -->

<div id="app"></div>

app.mount('#app')

<!-- we can write our root component's 
template directly inside 
the mount container -->

<div id="app">
    <button @click="count++">{{ count }}</button>
  </div>

  import { createApp } from 'vue'
  
  const app = createApp({
    data() {
      return {
        count: 0
      }
    }
  })
  
  app.mount('#app')

<!-- Configuration -->
<!-- For Error Handler -->

app.config.errorHandler = (err) => {
    /* handle error */
  }

<!-- There can be Multiple App in one page -->

const app1 = createApp({
    
  })
  app1.mount('#container-1')
  
  const app2 = createApp({
    
  })
  app2.mount('#container-2')