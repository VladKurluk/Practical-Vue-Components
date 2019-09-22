<template>
  <div class="home">
    <app-button :to="{ name: 'signin' }" />
    <app-button :to="{ name: 'signin' }" theme="danger" size="large" />
    <app-button @click.prevent="clicked" />
  </div>
</template>

<script>
// @ is an alias to /src
import AppButton from '@/components/AppButton.vue'

export default {
  name: 'home',
  components: {
    AppButton
  },
  methods: {
    clicked () {
      alert('Clickkkk!')
    }
  }
}
</script>
