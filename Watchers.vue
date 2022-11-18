
<!-- Watchers -->

export default {
    data() {
      return {
        question: '',
        answer: 'Questions usually contain a question mark. ;-)'
      }
    },
    watch: {
      // whenever question changes, this function will run
      question(newQuestion, oldQuestion) {
        if (newQuestion.includes('?')) {
          this.getAnswer()
        }
      }
    },
    methods: {
      async getAnswer() {
        this.answer = 'Thinking...'
        try {
          const res = await fetch('https://yesno.wtf/api')
          this.answer = (await res.json()).answer
        } catch (error) {
          this.answer = 'Error! Could not reach the API. ' + error
        }
      }
    }
  }
  
  <p>
    Ask a yes/no question:
    <input v-model="question" />
  </p>
  <p>{{ answer }}</p>

  <!-- Deepp Watchers -->

  export default {
    watch: {
      someObject: {
        handler(newValue, oldValue) {
          // Note: `newValue` will be equal to `oldValue` here
          // on nested mutations as long as the object itself
          // hasn't been replaced.
        },
        deep: true
      }
    }
  }

  <!-- Eager Watchers -->

  export default {
    // ...
    watch: {
      question: {
        handler(newQuestion) {
          // this will be run immediately on component creation.
        },
        // force eager callback execution
        immediate: true
      }
    }
    // ...
  }
  