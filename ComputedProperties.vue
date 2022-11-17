
<!-- computed property -->

export default {
    data() {
      return {
        author: {
          name: 'Hari Messi',
          books: [
            'Mass Man - Advanced Guide',
            'Hero - Basic Guide',
            'Don uh - The Mystery'
          ]
        }
      }
    },
    computed: {
      // a computed getter
      publishedBooksMessage() {
        // `this` points to the component instance
        return this.author.books.length > 0 ? 'Yes' : 'No'
      }
    }
  }
  template
  <p>Has published books:</p>
  <span>{{ publishedBooksMessage }}</span>

<!-- Writable Computed -->

  export default {
    data() {
      return {
        firstName: 'Hari',
        lastName: 'Messi'
      }
    },
    computed: {
      fullName: {
        // getter
        get() {
          return this.firstName + ' ' + this.lastName
        },
        // setter
        set(newValue) {
          // Note: we are using destructuring assignment syntax here.
          [this.firstName, this.lastName] = newValue.split(' ')
        }
      }
    }
  }
  
