<template>
  <div class="title">
    <h1>{{ label.toUpperCase() }}</h1>
  </div>
  
  <div class="underline"></div>
</template>

<script>
export default {
  name: 'Title',
  props: {
    label: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.title h1{
    font-size: 1.5rem;
    font-weight: 600;
    color: #fff;
    margin-bottom: 1rem;
    z-index: 3;
}
.underline{
    background: #ff8000;
    height: 2px;
    width: 4rem;
    border-radius: 8px;
}
</style>