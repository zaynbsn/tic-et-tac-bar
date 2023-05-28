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
  border: 1px solid #fff;
  border-radius: 8px;
  padding: 0.6rem 1.2rem;
  text-decoration: none;
  color: black;
  font-size: 1rem;
  letter-spacing: 0.05em;
  transition: all 200ms ease-in-out;
  box-shadow: 0 0 40px 40px #fff inset, 0 0 0 0 #fff;
}
.main-button:hover{
  box-shadow: 0 0 0px 0 #fff inset, 0 0 0px 0px #fff;
  color: #fff!important;
  background-color: transparent!important;
}
</style>