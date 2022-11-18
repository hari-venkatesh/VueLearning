
<!-- Registering Lifecycle Hooks -->

export default {
    beforeCreate() {
      console.log(`the component is now going to create.`)
    }
  }

  export default {
    created() {
      console.log(`the component is now created.`)
    }
  }
  
  export default {
    beforeMount() {
      console.log(`the component is now beforeMount.`)
    }
  }
  
  export default {
    mounted() {
      console.log(`the component is now mounted.`)
    }
  }
  
  export default {
    beforeUpdate() {
      console.log(`the component is now beforeUpdate.`)
    }
  }
  
  export default {
    updated() {
      console.log(`the component is now updated.`)
    }
  }
  export default {
  beforeUnmount() {
    console.log(`the component is now beforeUnmounte.`)
  }
}

  
  export default {
  unmounted() {
    console.log(`the component is now unmounted.`)
  }
}

