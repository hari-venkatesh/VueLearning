
<!-- v-for -->

data() {
    return {
      items: [{ message: 'Foo' }, { message: 'Bar' }]
    }
  }

  <li v-for="item in items">
    {{ item.message }}
  </li>

data() {
    return {
      parentMessage: 'Parent',
      items: [{ message: 'Foo' }, { message: 'Bar' }]
    }
  }

  <li v-for="(item, index) in items">
    {{ parentMessage }} - {{ index }} - {{ item.message }}
  </li>
  
  <li v-for="{ message } in items">
    {{ message }}
  </li>
  
  <!-- with index alias -->
  <li v-for="({ message }, index) in items">
    {{ message }} {{ index }}
  </li>
  
  <!-- v-for with an Object -->

  data() {
    return {
      myObject: {
        title: 'How to do lists in Vue',
        author: 'Jane Doe',
        publishedAt: '2016-04-10'
      }
    }
  }
  
  <ul>
    <li v-for="value in myObject">
      {{ value }}
    </li>
  </ul>
  
  <li v-for="(value, key, index) in myObject">
    {{ index }}. {{ key }}: {{ value }}
  </li>
  
  <ul>
    <template v-for="item in items">
      <li>{{ item.msg }}</li>
      <li class="divider" role="presentation"></li>
    </template>
  </ul>
  
<li v-for="todo in todos" v-if="!todo.isComplete">
    {{ todo.name }}
  </li>
  
  <MyComponent
  v-for="(item, index) in items"
  :item="item"
  :index="index"
  :key="item.id"
/>

data() {
  return {
    numbers: [1, 2, 3, 4, 5]
  }
},
computed: {
  evenNumbers() {
    return this.numbers.filter(n => n % 2 === 0)
  }
}
