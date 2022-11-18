
<!-- Components Basics -->

<!-- Defining a Component -->

<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>

<template>
  <button @click="count++">You clicked me {{ count }} times.</button>
</template>

export default {
    data() {
      return {
        count: 0
      }
    },
    template: `
      <button @click="count++">
        You clicked me {{ count }} times.
      </button>`
  }
  
  <!-- Using An Component -->

  <script>
import ButtonCounter from './ButtonCounter.vue'

export default {
  components: {
    ButtonCounter
  }
}
</script>

<template>
  <h1>Here is a child component!</h1>
  <ButtonCounter />
</template>

<!-- Listening To Events -->

data() {
    return {
      posts: [
        /* ... */
      ],
      postFontSize: 1
    }
  }
  
  <div :style="{ fontSize: postFontSize + 'em' }">
    <BlogPost
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
     />
  </div>
  
  <!-- BlogPost.vue, omitting <script> -->

<template>
    <div class="blog-post">
      <h4>{{ title }}</h4>
      <button>Enlarge text</button>
    </div>
  </template>
  