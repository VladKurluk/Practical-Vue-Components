<template>
  <router-link 
    class="btn" 
    :to="to"
    :class="[
      themes[theme], sizes[size]
    ]"
  >
    {{to.name}}
  </router-link>
</template>

<script>
export default {
  data: () => ({
    themes: {
      primary: 'btn-primary',
      danger: 'btn-danger',
    },
    sizes: {
      normal: '',
      large: 'btn-lg'
    }
  }),
  props: {
    // Color style props
    theme: {
      required: false,
      type: String,
      default: 'primary'
    },
    // Size props
    size: {
      required: false,
      type: String,
      default: 'normal'
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