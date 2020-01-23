<template>
  <a
    :href="link"
  >
    <slot />
  </a>
</template>

<script>
export default {
  props: {
    link: {
      required: true
    }
  }
}
</script>

<style lang="scss">
</style>