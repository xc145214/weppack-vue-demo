<template>
    <h1>数据语法绑定</h1>

    <h2>插值</h2>

    <p>
        <span>Message: {{ msg }}</span> <br>

        <span>This will never change: {{* msg }}</span>
    </p>

</template>

<script>
export default {
  data () {
    return {
      msg: 'Hello world!'
    }
  }

}
</script>

<style>

</style>