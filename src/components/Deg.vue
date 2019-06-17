<template>
  <h1>
    <span>{{ base }}</span>
    <sup>{{exp}}</sup>
    = {{ base ** exp }}
  </h1>
</template>

<script>
export default {
  name: "Deg",
  props: {
    base: Number,
    exp: Number
  }
};
</script>

