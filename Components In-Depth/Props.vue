
<!-- Props Declaration -->

<!-- Array Props Declaration -->

export default {
    props: ['foo'],
    created() {
      // props are exposed on `this`
      console.log(this.foo)
    }
  }

  <!-- Object Props Declaration -->
  
  export default {
    props: {
      title: String,
      likes: Number
    }
  }
  
  <!-- Prop Passing Details -->

  export default {
    props: {
      greetingMessage: String
    }
  }
  
  <span>{{ greetingMessage }}</span>

  <MyComponent greeting-message="hello" />

  <!-- Prop Validation -->

  class Person {
    constructor(firstName, lastName) {
      this.firstName = firstName
      this.lastName = lastName
    }
  }
  
  export default {
    props: {
      author: Person
    }
  }
  