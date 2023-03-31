<template>
  <h1>Hello</h1>
</template>

<script>
  import HelloWorld from '../components/HelloWorld'

  export default {
    name: 'Home',

    components: {
      HelloWorld,
    },
    props: {
      search: Function
    }
  }
</script>
