
<!-- Declaring Reactive State -->

export default {
    data() {
      return {
        count: 1
      }
    },
  
    // `mounted` is a lifecycle hook which we will explain later
    mounted() {
      // `this` refers to the component instance.
      console.log(this.count) // => 1
  
      // data can be mutated as well
      this.count = 2
    }
  }

<!-- DOM Update Timing -->

import { nextTick } from 'vue'

export default {
  methods: {
    increment() {
      this.count++
      nextTick(() => {
        // access updated DOM
      })
    }
  }
}

<!-- In Vue, state is deeply reactive 
by default. This means you can 
expect changes to be detected 
even when you mutate nested 
objects or arrays -->

export default {
    data() {
      return {
        obj: {
          nested: { count: 0 },
          arr: ['foo', 'bar']
        }
      }
    },
    methods: {
      mutateDeeply() {
        // these will work as expected.
        this.obj.nested.count++
        this.obj.arr.push('baz')
      }
    }
  }