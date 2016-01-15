<template>
  <div class="example">{{ msg }}</div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Hello this is component A!'
    }
  }
}
</script>

<style>
.example {
  color: red;
}
</style>