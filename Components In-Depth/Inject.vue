
<!-- Prop Drilling -->

export default {
    provide: {
      message: 'hello!'
    }
  }

  export default {
    data() {
      return {
        message: 'hello!'
      }
    },
    provide() {
      return {
        message: this.message
      }
    }
  }
  
  <!-- App Level Provide -->

  import { createApp } from 'vue'

const app = createApp({})

app.provide(/* key */ 'message', /* value */ 'hello!')

export default {
    inject: ['message'],
    created() {
      console.log(this.message) // injected value
    }
  }

  export default {
    inject: ['message'],
    data() {
      return {
        // initial data based on injected value
        fullMessage: this.message
      }
    }
  }
  
  <!-- Injection Aliasing -->

  export default {
    inject: {
      /* local key */ localMessage: {
        from: /* injection key */ 'message'
      }
    }
  }

  
  import { computed } from 'vue'

  export default {
    data() {
      return {
        message: 'hello!'
      }
    },
    provide() {
      return {
        message: computed(() => this.message)
      }
    }
  }
  