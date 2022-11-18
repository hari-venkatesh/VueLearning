
<!-- Attribute Inheritance -->

<!-- template of <MyButton> -->

    <button>click me</button>

    <MyButton class="large" />

    <!-- Final -->

    <button class="large">click me</button>

<!-- template of <MyButton> -->

    <button class="btn">click me</button>

    <button class="btn large">click me</button>

    <MyButton @click="onClick" />

<!-- template of <MyButton/> that simply renders another component -->

    <BaseButton />

<!-- Disabling Attribute Inheritance -->

<span>Fallthrough attributes: {{ $attrs }}</span>

<div class="btn-wrapper">
    <button class="btn">click me</button>
  </div>
  
  export default {
    created() {
      console.log(this.$attrs)
    }
  }
  