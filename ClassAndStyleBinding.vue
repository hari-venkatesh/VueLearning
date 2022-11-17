
<!-- Binding HTML Classes -->

<div :class="{ active: isActive }"></div>

data() {
    return {
      isActive: true,
      hasError: false
    }
  }

  <div
  class="static"
  :class="{ active: isActive, 'text-danger': hasError }"
></div>

<div class="static active"></div>

data() {
    return {
      classObject: {
        active: true,
        'text-danger': false
      }
    }
  }

  <div :class="classObject"></div>

  data() {
    return {
      isActive: true,
      error: null
    }
  },
  computed: {
    classObject() {
      return {
        active: this.isActive && !this.error,
        'text-danger': this.error && this.error.type === 'fatal'
      }
    }
  }

  <div :class="classObject"></div>

<!-- Binding to Arrays -->

data() {
    return {
      activeClass: 'active',
      errorClass: 'text-danger'
    }
  }
  
  <div :class="[activeClass, errorClass]"></div>

  <div class="active text-danger"></div>

  <div :class="[isActive ? activeClass : '', errorClass]"></div>

  <div :class="[{ active: isActive }, errorClass]"></div>

<!-- Binding Inline Styles -->

data() {
    return {
      activeColor: 'red',
      fontSize: 30
    }
  }

  <div :style="{ color: activeColor, fontSize: fontSize + 'px' }"></div>

  <div :style="{ 'font-size': fontSize + 'px' }"></div>

  data() {
    return {
      styleObject: {
        color: 'red',
        fontSize: '13px'
      }
    }
  }
  
  <div :style="[baseStyles, overridingStyles]"></div>
