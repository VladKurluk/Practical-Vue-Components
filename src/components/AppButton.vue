<template>
  <router-link 
    class="btn"
    @click.native="clicked"
    :disabled="disabled"
    :to="to"
    :class="[
      themes[theme], sizes[size], {
        'disabled': disabled
      }
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
    // Disabled stste 
    disabled: {
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
  },
  methods: {
    clicked (e) {
      this.$emit('click', e)
    }
  }
}
</script>