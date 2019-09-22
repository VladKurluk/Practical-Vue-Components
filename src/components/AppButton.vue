<template>
  <router-link 
    class="btn" 
    :to="to"
    :class="{
      'btn-primary': primary,
      'btn-danger': danger,
      '': normal,
      'btn-lg': large
    }"
  >
    {{to.name}}
  </router-link>
</template>

<script>
export default {
  props: {
    // Color style props
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
    // Size props
    normal: {
      required: false,
      type: Boolean,
      default: true
    },
    large: {
      required: false,
      type: Boolean,
      default: false
    },
    // Navigate to props
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