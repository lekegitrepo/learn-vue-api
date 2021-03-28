<template>
  <div>
    <h1>Vue Api references</h1>
  </div>
</template>

<script>
export default {
  name: 'api-reference',
  props: {
    msg: String
  },
  data() {
    return {
      a: 1,
      b: 2,
      c: {
        d: 3,
        e: 4
      }
    }
  },
  created() {
    // top-level property name
    this.$watch('a', (newVal, oldVal) => {
      // do something
    })

    // function for watching a single nested property
    this.$watch(
      () => this.c.d,
      (newVal, oldVal) => {
        // do something
      }
    )

    // function for watching a complex expression
    this.$watch(
      // every time the expression `this.a + this.b` yields a different result,
      // the handler will be called. It's as if we were watching a computed
      // property without defining the computed property itself
      () => this.a + this.b,
      (newVal, oldVal) => {
        // do something
      }
    )
  }
}
</script>
