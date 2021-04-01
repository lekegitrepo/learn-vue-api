<template>
  <div>
    <h1>Vue Api references</h1>
    <p>{{a}}</p>
    <button type="button" name="button" v-on:click="increase">count</button>
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
      },
      article: {
        text: 'Vue is awesome!'
      },
      comments: ['Indeed!', 'I agree']
    }
  },
  created() {
    // top-level property name
    this.$watch('a', (newVal, oldVal) => {
      // do something
      console.log('This is new val', newVal, 'This is old val', oldVal)
    })

    // function for watching a single nested property
    this.$watch(
      () => this.c.d,
      (newVal, oldVal) => {
        // do something
        console.log('function for watching a single nested property:','This is new val', newVal, 'This is old val', oldVal)
      }
    )

    // function for watching a complex expression
    this.$watch(
      // every time the expression `this.a + this.b` yields a different result,
      // the handler will be called. It's as if we were watching a computed
      // property without defining the computed property itself
      () => this.a + this.b,
      (newVal, oldVal) => {
        console.log('function for watching a complex expression:','This is new val', newVal, 'This is old val', oldVal)
      }
    )
  },
  methods: {
    increase(){
      if(this.a <= 5) {
        this.a += 1
      }
    }
  }
}
</script>
