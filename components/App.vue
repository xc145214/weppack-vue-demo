<template>
    <div class="app">
        <component-a></component-a>
        <component-b></component-b>
        <component-bind></component-bind>
    </div>
</template>



<script>
import ComponentA from './ComponentA.vue'
import ComponentB from './ComponentB.vue'
import ComponentBind from './ComponentBind.vue'

export default {
  components: {
    ComponentA,
    ComponentB,
    ComponentBind
  }
}
</script>
