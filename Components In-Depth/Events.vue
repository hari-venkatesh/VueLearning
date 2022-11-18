
<!-- Emitting and Listening to Events -->

<!-- MyComponent -->

<button @click="$emit('someEvent')">click me</button>

export default {
    methods: {
      submit() {
        this.$emit('someEvent')
      }
    }
  }
  
  <!-- Event Arguments -->

  <button @click="$emit('increaseBy', 1)">
    Increase by 1
  </button>
  
  <MyButton @increase-by="(n) => count += n" />

  <MyButton @increase-by="increaseCount" />

  methods: {
  increaseCount(n) {
    this.count += n
  }
}

<!-- CustomInput.vue -->

<script>
export default {
  props: ['modelValue'],
  emits: ['update:modelValue'],
  computed: {
    value: {
      get() {
        return this.modelValue
      },
      set(value) {
        this.$emit('update:modelValue', value)
      }
    }
  }
}
</script>

<template>
  <input v-model="value" />
</template>

<MyComponent v-model:title="bookTitle" />
