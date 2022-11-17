
<!-- Listening to Events -->

<!-- Inline handlerss -->

data() {
    return {
      count: 0
    }
  }

  <button @click="count++">Add 1</button>
<p>Count is: {{ count }}</p>

<!-- Method handlerss -->

methods: {
    say(message) {
      alert(message)
    }
  }
  
  <button @click="say('hello')">Say hello</button>
<button @click="say('bye')">Say bye</button>

<!-- using $event special variable -->
<button @click="warn('Form cannot be submitted yet.', $event)">
    Submit
  </button>
  
  <!-- using inline arrow function -->
  <button @click="(event) => warn('Form cannot be submitted yet.', event)">
    Submit
  </button>

methods: {
    warn(message, event) {
      // now we have access to the native event
      if (event) {
        event.preventDefault()
      }
      alert(message)
    }
  }

<!-- Event Modifier -->

<!-- the click event's propagation will be stopped -->
<a @click.stop="doThis"></a>

<!-- the submit event will no longer reload the page -->
<form @submit.prevent="onSubmit"></form>

<!-- modifiers can be chained -->
<a @click.stop.prevent="doThat"></a>

<!-- just the modifier -->
<form @submit.prevent></form>

<!-- only trigger handler if event.target is the element itself -->
<!-- i.e. not from a child element -->
<div @click.self="doThat">...</div>
