<template>
  <a class="main-button" :href="to" :target="blank ? '_blank': ''">{{ label }}</a>
</template>

<script>
export default {
  name: 'Button',
  props: {
    to: {
      type: String,
      required: true
    },
    label: {
      type: String,
      required: true
    },
    blank:{
      type: Boolean,
      required: false,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.main-button{
  width: fit-content;
  height: fit-content;
  background-color: #fff;
  border-radius: 8px;
  padding: 0.6rem 1.2rem;
  text-decoration: none;
  color: black;
  font-size: 1rem;
  letter-spacing: 0.05em;
}
</style>