<template>
  <router-link 
    class="btn" 
    :to="to"
    :class="{
      'btn-primary': primary,
      'btn-danger': danger,
    }"
  >
    {{to.name}}
  </router-link>
</template>

<script>
export default {
  props: {
    primary: {
      required: false,
      type: Boolean,
      default: true
    },
    danger: {
      required: false,
      type: Boolean,
      default: false
    },
    to: {
      required: false,
      type: Object,
      default () {
        return {
          name: 'home'
        }
      }
    }
  }
}
</script>